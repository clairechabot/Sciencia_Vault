---
Purchased:
  "{ date }": 
projects: 
company: 
Price: 
URL: 
tags:
  - lab_inventory
summary:
---

 [[Lab Inventory MOC]] 

---

# Specs
- 


---

# Related items

_List any other affiliated Inventory items here._

-  

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