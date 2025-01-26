---
aliases: []
tags: [MOC]
title: Work Notes MOC
date_created: 2024-03-04-Monday
date_modified: 2024-06-17-Monday
banner: "![[women-students-attend-a-lecture-in-the-general-lecture-room-at-the-medical-college-for-women-on-east-twelfth-street-and-second-avenue-new-york-usa-after-an-illustration-from-an-1870-edition-of-frank-leslies-il.jpg]]"
banner_y: 0.508
---

[[Dashboard]]

%%**Template:** [[Daily Note]]%%

---

_This page conglomerates all of the Work Notes (i.e. Daily Notes) in "100 Lab Notes/Work Notes" that are made on a daily basis. These notes can be linked to [[People MOC]] as well as [[Meetings MOC]]. "100 Lab Notes/Work Notes" are automatically sorted within the approiate year and month the daily note is created. _

<br>

```meta-bind-button
label: New Work Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: command
    command: workspace:new-tab
  - type: command
    command: daily-notes

```



<br>

---

_I like having this tracker to feel a sense of accomplishment for the amount of work I've done so far. I think it'll be neat to see at the end of my Ph.D.!_

```tracker
searchType: frontmatter
searchTarget: Hours_Worked
folder: 100 Lab Notes/Work Notes
dateFormat: "YYYY-MM-DD-dddd"
summary:
    template: "I've worked {{sum()}} hours on my Ph.D.!"
    style: "font-size:35px;color:green;margin-left: 50px;margin-top:00px;"
```


---

# List of Work Notes

_The following dataview callouts organise the Work Notes by year. For a new year, simply copy and paste and change the year within the WHERE section of the callout. These are organised in descending order._

<br>

## 2025

```dataview
TABLE created AS "Date", location AS "Location", Hours_Worked AS "Hours Worked"
FROM "100 Lab Notes/Work Notes" and -#MOC
SORT created DESC
WHERE contains(file.name, "2025")
```

## 2024

```dataview
TABLE created AS "Date", location AS "Location", Hours_Worked AS "Hours Worked"
FROM "100 Lab Notes/Work Notes" and -#MOC
SORT created DESC
WHERE contains(file.name, "2024")
```
