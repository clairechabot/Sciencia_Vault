---
aliases: 
cssclasses:
  - table-wide
tags:
  - MOC
title: Course MOC
date_created: 2024-04-06-Saturday
date_modified: 2024-06-13-Thursday
banner: "![[undefined - Imgur (1).jpg]]"
banner_y: 0.448
---

[[Dashboard]]
%%**Template**: [[Course Note Template]]%%

---

```ad-quote
_"The beautiful thing about learning is that no one can take it away from you."_ - **B.B. King**
```

```meta-bind-button
label: New Course MOC
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Course MOC Template.md
    folderPath: 200 Courses
    fileName: ""
    openNote: true
```

This will be used to organize all of my course notes by the class, then the folders and tags relevant to different topics in each class. It will act as a hub for you to find information from the notes I've taken. These notes will also be linked to [[People MOC]] that links the person's giving the course you're attending. 

<br>

# Current Courses

_The classes are Sorted alphabetically. Any class with stats = ongoing in the frontmatter will be displayed here._

<br> 

```dataview 
TABLE Year, Description
FROM "200 Courses" AND #MOC 
WHERE status = "ongoing"
SORT file.name asc 
```

<br>

---

# Homework

_Any tasks placed in a note in the "200 Courses" folder will appear here as homework. It will be group by the notes associated MOC in its frontmatter (ie. the MOC for the class the note is associated with)._
<br>

```dataview 
TASK
FROM "200 Courses"
WHERE !completed 
GROUP BY MOC
SORT MOC ASC
```

---

# All Courses

_Sorted by most recently taken._The classes are Sorted alphabetically. Any class in "200 Courses" will be displayed here._
<br>

```dataview 
TABLE Year, Description
FROM "200 Courses" AND #MOC
SORT file.ctime desc 

```

<br>
