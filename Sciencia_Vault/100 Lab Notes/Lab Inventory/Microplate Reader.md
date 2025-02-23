---
aliases:
  - microplate reader
tags:
  - lab_inventory
Purchased: 2023-10-15
Price: $5,000
company:
  - BioTech Instruments
URL: https://www.biotechinstruments.com/microplate-reader
title: 2023-10-15 Microplate Reader
date_created: 2023-10-15-Sunday
date_modified: 2024-01-10-Wednesday
projects:
  - "[[RNA in Situ High-Throughput Protocol Development]]"
summary: A microplate reader used for measuring optical density (OD) in 96-well plates for enzymatic assays.
---

[[Lab Inventory MOC]]

---

# Specs

- Model: XR-500
- Wavelength Range: 340–850 nm
- Capacity: 96 wells
- Compatible Software: SoftMax Pro

---

# Related items

_List any other affiliated Inventory items here._

- [[Pipette Set (Adjustable)]]
- [[96-Well Plate (Standard)]]  
- [[Enzyme Kinetics Assay Protocol]]  

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

- Calibrated on 2024-01-05 for use with enzymatic assays.
- Requires maintenance every 6 months.


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
