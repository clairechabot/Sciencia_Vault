---
aliases: 
mapofcontent: yes
status: ongoing
summary: Curing cancer.
start_date: 2024-06-10
end_date: 
tags:
  - MOC
  - PhD_project
collaborators:
  - "[[Albert Einstein]]"
  - "[[Marie Curie]]"
title: RNA in situ Protocol Dev MOC
date_created: 2024-06-27-Thursday
date_modified: 2024-06-27-Thursday
---

[[Ph.D. Dashboard]]

%% [[Project MOC Template]] %%


---

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

<br> 


```ad-abstract
title: Project Summary

_Summarise why you're doing this project here and what is the overarching goal._

```

<br>

---

# Experiments

```ad-note
title: Ongoing
collapse: open

``````dataview
TABLE 
FROM #experiment 
WHERE status ="ongoing" AND contains(file.outlinks, [[]])
SORT file.ctime asc 
```

```ad-question
title: Someday
collapse: closed
```dataview
TABLE 
FROM #experiment 
WHERE status ="someday" AND contains(file.outlinks, [[]])
SORT file.ctime asc 
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

```dataview 
TABLE startdate AS "Scheduled", summary AS "Summary"
FROM "100 Lab Notes/Meetings" 
WHERE contains(file.outlinks, [[]])
SORT file.cdate DESC
```

<br>

---

# Project Notes

```dataview 
TABLE summary AS "Summary"
FROM "100 Lab Notes/Projects/Example Project/Project Notes"
SORT file.name asc
```

---

# Protocols

_Protocols with this project hyperlinked will appear in the dataview callout below._

```dataview
TASK 
FROM "100 Lab Notes/Projects"  
WHERE econtains(tags, "#protocol") AND contains(file.outlinks, [[]])
SORT file.name DESC
```
