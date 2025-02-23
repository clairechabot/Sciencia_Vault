---
location: 
Hours_Worked: 
tags:
  - work_note
  - PhD
Icon: 
pomodoros: 
created: <% tp.date.now("YYYY-MM-DD") %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
---

[[Dashboard]] | [[Work Notes MOC]]

---

<< [[100 Lab Notes/Work Notes/<%tp.date.now("YYYY", -1) %>/<% tp.date.now("MM-MMMM", -1) %>/<% tp.date.now("YYYY-MM-DD-dddd", -1) %> | Yesterday]] | [[100 Lab Notes/Work Notes/<%tp.date.now("YYYY", 1) %>/<% tp.date.now("MM-MMMM", 1) %>/<% tp.date.now("YYYY-MM-DD-dddd", 1) %> | Tomorrow]] >>

_This allows you to move back and forth between dates of your daily note. If no date exists, then a daily note is created for said date when the button is clicked. However, the daily note / work note template won't be applied._

___

### This Day Last Year 

![[<% tp.date.now("YYYY-MM-DD", "P-1Y") %>]]

---


## To-Do List 
<br> 

- 



<br> 
<br>

________

# Notes
<br> 

_In the frontmatter, under "Icon", if you include "important_date" then the title of this daily note will become red. This makes it stand out more within the list in [[Work Notes MOC]] in case you need to quickly reference it in the future._ An example of this has been made on [[2024-12-16-Monday]]. 


<br> 
<br>

---

_These callouts show any notes that you made or edited (ie. touched) on the day the daily note was created. I find this useful when I can't remember where I put a note, but do remember the day I worked on it._

### Notes created today
```dataview
List 
FROM "" 
WHERE file.cday = this.file.day
SORT file.ctime asc
```

<br> 

### Notes last touched today
```dataview
List 
FROM "" 
WHERE file.mday = this.file.day
SORT file.mtime asc
```

