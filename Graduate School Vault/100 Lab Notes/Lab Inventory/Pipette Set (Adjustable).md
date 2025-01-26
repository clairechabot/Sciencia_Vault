---
aliases:
  - pipette set
tags:
  - lab_inventory
Purchased: 2022-05-01
Price: $1,200
company:
  - Eppendorf
URL: https://www.eppendorf.com/pipettes
title: 2022-05-01 Adjustable Pipette Set
date_created: 2022-05-01-Sunday
date_modified: 2024-01-26-Friday
projects:
  - "[[RNA in Situ High-Throughput Protocol Development]]"
summary: A set of adjustable pipettes for precise liquid handling (0.1–1000 µL).
---

[[Lab Inventory MOC]]

---

# Specs

- **Brand**: Eppendorf Research Plus
- **Volumes**: 0.1–2.5 µL, 10–100 µL, 100–1000 µL
- **Autoclavable**: Yes
- **Accuracy**: ±0.1 µL at low volumes

---

# Related items

_List any other affiliated Inventory items here._

- [[Pipette Tips (0.1–1000 µL)]]
- [[Cell Culture Media Preparation Protocol]]

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

- Serviced on 2023-12-20.
- Use only with compatible pipette tips.

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
