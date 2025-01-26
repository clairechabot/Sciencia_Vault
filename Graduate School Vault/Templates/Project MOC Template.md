---
mapofcontent: yes
status: ongoing
summary: 
start_date: {{date}}
end_date: 
tags:
  - MOC
  - PhD_project
collaborators:
---

[[Dashboard]] 

%% [[Project MOC Template]] %% 


---

_For the buttons below, you will need to change where the new experiments are going, which project folder they belong to. Check the folderpath._

<br> 

> [!col]
>
> > [!col-md]
> >
> > ```meta-bind-button
> > label: New Project Note
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: primary
> > actions:
> >   - type: templaterCreateNote
> >     templateFile: Templates/Project Note Template.md
> >     folderPath: 100 Lab Notes/Projects/Example Project/Project Notes
> >     fileName: New Note
> >     openNote: true
> > ```
>
> > [!col-md]
> >
> > ```meta-bind-button
> > label: New Project Experiment
> > icon: ""
> > hidden: false
> > class: ""
> > tooltip: ""
> > id: ""
> > style: primary
> > actions:
> >   - type: templaterCreateNote
> >     templateFile: Templates/Experiment Template.md
> >     folderPath: 100 Lab Notes/Projects/Example Project/Experiments
> >     fileName: New Note
> >     openNote: true
> > ```

```ad-abstract
title: Project Summary

_Insert a short summary of the project here._
- Why am I doing this project 
- What is the hypothesis 

```

---

# Experiments

_Experiments with this project hyperlinked in the frontmatter (project=this.file.name) will appear in the dataview callout below. They will then be organised based on their status: ongoing, someday, and failed._

```ad-note
title: Ongoing
collapse: open

```dataview 
TABLE file.ctime AS "Date Started", file.mtime AS "Last Modified", summary AS "Summary", id AS "ID"
FROM "100 Lab Notes" and "#experiment"
WHERE 
	status="ongoing" 
	AND project=this.file.name
SORT file.ctime asc 
```

```ad-question
title: Someday
collapse: closed
```dataview 
LIST 
FROM "100 Lab Notes" AND #experiment 
WHERE 
	contains(status, "someday")
	AND contains(file.outlinks, [[]])
SORT file.cdate asc
LIMIT 10
```

```ad-summary
title: Finished Experiments
collapse: closed
```dataview 
LIST 
FROM "100 Lab Notes" AND #experiment 
WHERE 
	contains(status, "failed")
	OR contains(status, "done")
	AND contains(file.outlinks, [[]])
SORT file.cdate asc
LIMIT 10
```

<br> 

---

# Project Meetings

_When a meeting has this file name hyperlinked in its frontmatter under "projects", those meetings will appear in the dataview callout below._ 

```dataview 
TABLE startdate as Scheduled, summary AS "Summary"
FROM "100 Lab Notes/Meetings" 
WHERE contains(file.outlinks, [[]])
SORT file.name asc 
```

<br>

---

# Project Notes

```dataview 
TABLE summary AS "Summary"
FROM "100 Lab Notes/Projects/Example Project/Project Notes"
SORT file.name asc
```

<br>

---

# Topic MOCs

_Any literature topics you have created that have this project MOC hyperlinked will appear in the dataview callout below._

```dataview
TABLE summary AS "Summary", projects AS "Associated Projects"
FROM "100 Lab Notes/Topic MOCs" 
WHERE contains(file.outlinks, [[]]) 
SORT file.cday DESC
```

<br>

---

# Protocols

_Protocols with this project hyperlinked will appear in the dataview callout below._

```dataview
TASK 
FROM "100 Lab Notes/Projects"  
WHERE econtains(tags, "#protocol") AND contains(file.outlinks, [[]])
SORT file.name DESC
```


