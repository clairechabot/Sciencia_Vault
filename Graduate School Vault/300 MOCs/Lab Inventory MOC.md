---
aliases: []
tags: [MOC]
title: Lab Inventory MOC
date_created: 2024-03-07-Thursday
date_modified: 2024-06-13-Thursday
banner: "![[Google-library.jpg]]"
banner_y: 0.212
---


[[Dashboard]]
%%**Template**: [[Lab Inventory Template]]%%


---

This was developed to streamline the location of supplies and equipment in their workspace. By implementing this organized system, you can dedicate more focus to their research tasks, minimizing the time spent searching for items. It can also be linked to the [[People MOC]] and [[Protocol MOC]] and a Project MOC.

<br>

```meta-bind-button
label: New Item
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
    folderPath: 100 Lab Notes/Lab Inventory
    fileName: New Item
    openNote: true

```

<br>

---

<br>

```dataview
table Purchased, company AS "Company", projects AS "Projects"
FROM "100 Lab Notes/Lab Inventory"
SORT Purchased desc
```
