---
aliases: 
tags:
  - lab_inventory
Purchased: 2025-01-26
Price: 
company:
  - Company 2
URL: 
title: 2024-03-09 Test Item
date_created: 2024-03-09-Saturday
date_modified: 2024-06-13-Thursday
projects:
  - "[[Example Project MOC]]"
summary: This is a test item.
---

 [[Lab Inventory MOC]] 

---

# Specs
- 


---

# Related items

_List any other affiliated Inventory items here._

-  [[Test Item 1]]

<br> 

_Any items that have the current item referenced in it will appear here._

```dataview
TABLE summary AS "Summary"
FROM "100 Lab Notes/Lab Inventory" 
WHERE contains(file.outlinks, [[]])
SORT file.cday DESC
```

---

# Notes
 -


---
# Affiliated 

<br> 

## Projects 

_When you link an item within a project note, the affiliated projected note will show up here._

```dataview
TABLE summary AS "Summary", status AS "Status"
FROM "100 Lab Notes/Projects" 
WHERE contains(file.outlinks, [[]])
SORT file.cday DESC
```

<br>

## Protocols 

_Whenever you link an item within a protocol, the protocol will show up here in the callout._

```dataview
TABLE summary AS "Summary"
FROM "100 Lab Notes/Protocols" 
WHERE contains(file.outlinks, [[]])
SORT file.cday DESC
```

