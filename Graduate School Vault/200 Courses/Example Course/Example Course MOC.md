---
aliases: 
Year: 2024
Semester: Summer
Professor: "[[Marie Curie]]"
status: ongoing
MOC:
  - yes
tags:
  - course
  - MOC
  - SBMS
title: Example School MOC
date_created: 2024-06-07-Friday
date_modified: 2024-06-13-Thursday
Description: What is the course about?
---

[[Course MOC]] / [[Ph.D. Dashboard]]

---

```meta-bind-button
label: New Course Note
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
    folderPath: 200 Courses/Example Course/Study Notes
    fileName: New Note
    openNote: true

```

<br> 

```ad-note
title: Course Resources
collapse: closed

_Resources used for these notes._
```

<br>

## Class Notes

```dataview 
TABLE Lecturer, summary AS "Summary"
FROM "200 Courses/Example Course/Study Notes"
SORT file.ctime desc 

```

<br>
<br>

## Action Items

```dataview
TASK
FROM "200 Courses/Example Course"
WHERE !completed
GROUP BY file.link
SORT file.name asc
```
