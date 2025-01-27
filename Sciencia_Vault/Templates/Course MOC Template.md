---
Year: 
Semester: 
Description: 
Professor: 
status: 
MOC:
  - yes
tags:
  - course
  - MOC
---
[[Course MOC]]

---

```meta-bind-button
label: New Study Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: command
    command: workspace:new-tab
  - type: createNote
    folderPath: 200 Courses/NEW CLASS/Classes
    fileName: New Course Note
    openNote: true

```

_You will need to change the folder that the new study note goes into when you create a new Course MOC; look at folder path for the button where it says "NEW CLASS"._ 

<br>

```ad-note
title: Course Resources
collapse: closed

_Resources used for this class._

```

<br>

---

# Class Notes 

_Notes associated with the class. You do need to put the class MOC into each note's frontmatter for it to appear here._

<br> 

```dataview 
TABLE Date, Professor
FROM "200 Courses"
WHERE contains(file.outlinks, [[]])
SORT file.ctime desc 

```

<br>

---

# Tasks 

## To-do List

_Section to jot down any tasks associated with this class outside of a specific note._

- [ ] Course MOC Example task, no assigned date


<br> 

## Action Items

_Action items are incompleted tasks that were created within the associated class MOC. You do need to put the class MOC into each note frontmatter for it to appear here._

```dataview
TASK 
FROM "200 Courses"
WHERE 
	!completed 
	AND due.month = date(today).month 
	AND due.year = date(today).year 
	AND contains(file.outlinks, [[]])
SORT due asc
GROUP BY due
```


