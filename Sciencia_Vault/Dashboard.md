---
aliases: 
tags: 
cssclasses:
  - wide-page
title: Dashboard
date_created: 2024-04-20-Saturday
date_modified: 2024-06-20-Thursday
banner:
banner: "![[ndndhg2fdii61.jpg]]"
banner_y: 0.752
---

```widgets
type: clock
```

> [!col]
>
> > [!col-md]
> > ```meta-bind-button
> > label: Courses
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: primary
> > actions:
> >   - type: open
> >     link: "[[Course MOC]]"
> >     newTab: true
> > ```
> 
> > [!col-md]
> >
> > ```meta-bind-button
> > label: Daily Note
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: default
> > actions:
> >   - type: command
> >     command: daily-notes
> > ```
> 
> > [!col-md]
> >
> > ```meta-bind-button
> > label: Directory
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: primary
> > actions:
> >   - type: open
> >     link: "[[People MOC]]"
> >     newTab: true
> > ```
> 
> > [!col-md]
> >
> > ```meta-bind-button
> > label: Lab Inventory
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: default
> > actions:
> >   - type: open
> >     link: "[[Lab Inventory MOC]]"
> >     newTab: true
> > ```
> 
> > [!col-md]
> >
> > ```meta-bind-button
> > label: Meetings
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: primary
> > actions:
> >   - type: open
> >     link: "[[Meetings MOC]]"
> >     newTab: true
> > ```
> 
> > [!col-md]
> >
> > ```meta-bind-button
> > label: Protocols
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: default
> > actions:
> >   - type: open
> >     link: "[[Protocol MOC]]"
> >     newTab: true
> > ```

---
%% [[Dashboard]] // [[Protocol MOC]] // [[Meetings MOC]] // [[Protocol MOC]] // [[Lab Inventory MOC]] // [[People MOC]] %%

```ad-quote
_"I am among those who think that science has great beauty. A scientist in his laboratory is not only a technician: he is also a child placed before natural phenomena which impress him like a fairy tale."_ - **Marie Salomea Skłodowska-Curie**
%%
```

<br>

# Projects

%% This table includes all active projects. %%

<br>

```dataview 
TABLE file.ctime AS "Date Started", file.mtime AS "Last Modified", collaborators AS "Collaborators", summary AS "Summary"
FROM "100 Lab Notes/Projects" 
WHERE status="ongoing" AND mapofcontent="yes" 
SORT file.ctime asc 

// Dataview table for ongoing projects
```

<br>

# Upcoming Meetings

<br>

```dataview
TABLE location AS "Location", start_time AS "Start Time", summary
FROM "100 Lab Notes/Meetings" and -#MOC
WHERE status = "planned"
SORT startdate ASC, start_time ASC
```

<br>

---

# Tasks

```ad-abstract
title: Homework
collapse: open
```dataview  
TASK  
FROM "200 Courses" AND -#paperwork AND -#obsidian
WHERE !completed
GROUP BY path
SORT due ASC
```


## This Week
> > ```dataview
> > TASK 
> > FROM "100 Lab Notes" AND -#paperwork AND -#obsidian
> > WHERE !completed AND due.week = date(today).week AND due.year = date(today).year
> > SORT due ASC 
> > GROUP BY due
> > ```

##  Inbox

> > _These tasks have no due date and are not scheduled._
> >
> > ```dataview 
> > TASK
> > FROM "100 Lab Notes" AND -#obsidian AND -#paperwork AND -#to_read
> > WHERE !completed AND !scheduled AND !due 
> > SORT file.name asc
> > ```

<br> 

```ad-warning
title: Overdue
collapse: open
```dataview  
TASK  
FROM "100 Lab Notes" AND -#paperwork AND -#obsidian
WHERE due < date(today) & due != null AND !completed
SORT due asc
```

```ad-tldr
title: This Month's Tasks
collapse: closed
```dataview 
TASK 
FROM "100 Lab Notes" AND -#paperwork AND -#obsidian
WHERE !completed AND due.month = date(today).month AND due.year = date(today).year 
SORT due asc
GROUP BY due
```

```ad-note
title: Paperwork
collapse: closed

_Tasks labeled with "#paperwork" will appear in the query below._

```dataview 
TASK 
FROM #paperwork
WHERE !completed AND !due

```

```ad-check
title: Last 10 Completed Tasks
collapse: closed

_This query displays the last 10 tasks you've completed in descending order._

```dataview
TASK 
FROM "100 Lab Notes"
WHERE completed
SORT DESC
LIMIT 10
````

<br>

---

# Upcoming Classes

<br>

```dataview
TABLE Lecturer, location AS "Location", start_time AS "Start Time", summary
FROM "200 Courses"
WHERE status = "planned"
SORT startdate ASC, start_time ASC
```

<br>

---

# Papers to Read

_Any time you write down a paper as a task and add "#to_read" to it, it will appear in the following query._

<br>

```dataview 
TASK  
FROM #to_read 
WHERE !completed AND !due
```


<br>

---

# Finished Projects

_This table includes all completed projects that have the "status" in their frontmatter as "done"._

<br>

```dataview 
TABLE file.ctime AS "Date Started", end_date AS "Completed", Collaborators, summary AS "Summary"
FROM "100 Lab Notes/Projects"
WHERE 
	contains(status, "done")
	AND mapofcontent="yes" 
SORT file.cdate asc

```

<br>


```ad-success
title: Finished Experiments
collapse: closed

_This query contains the last 10 experiments that had the "status" in their frontmatter labeled as "done"._

```dataview 
TABLE file.ctime AS "Date Started", end_date AS "Completed", MOC AS "Project", Collaborators, summary AS "Summary"
FROM "100 Lab Notes/Projects" AND #experiment
WHERE contains(status, "done")
SORT file.cdate asc
LIMIT 10
```


```ad-fail
title: Failed Experiments
collapse: closed

_This query has the last 10 experiments with the "status" in their frontmatter labeled as "failed"._

```dataview 
TABLE file.ctime AS "Date Started", end_date AS "Closed On", MOC AS "Project", Collaborators, summary AS "Summary"
FROM "100 Lab Notes/Projects" AND #experiment
WHERE contains(status, "failed")
SORT file.cdate asc
LIMIT 10
```
