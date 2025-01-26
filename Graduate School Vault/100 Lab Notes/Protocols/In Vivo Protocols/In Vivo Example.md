---
aliases: 
tags:
  - protocol
title: Protocol Title
date_created: 2024-06-28-Friday
date_modified: 2024-06-28-Friday
created: 2024-06-28
summary: Protocol summary
Recommended_by:
  - "[[Marie Curie]]"
source: Source
projects:
  - "[[Example Project MOC]]"
protocol_type: In_Vivo
---

[[Protocol MOC]]/ [[Ph.D. Dashboard]] 

---


```ad-abstract
title: Purpose

Gotta get that blood.   

```

---

# Experiments  
%%The query will pull any projects that have used this protocol. Sorted by the last modified time of that experiment file.%% 

<br> 

```dataview
	LIST 
	FROM "100 Lab Notes/Projects" 
	WHERE contains(file.outlinks, [[]])
	GROUP BY file.link
	SORT file.mtime ASC
```

<br> 

---

# Lab Inventory Items
%%This query will pull any lab inventory items that are associated with this protocol. Sorted by the last modified time of that experiment file. %%
<br> 

```dataview
	LIST 
	FROM "100 Lab Notes/Lab Inventory" 
	WHERE contains(file.outlinks, [[]])
	GROUP BY file.link
	SORT file.mtime ASC
```

<br> 

---

# Relevant Papers 

<br> 




<br> 

---

# Protocol
%%Documentation of the actual protocol.%%

1. Centrifuge blood for serum collection (tube with white cap) 
	1. 2800 rpm
	2. 10 mins
	3. RT
2. Centrifuge blood for plasma collection (tube with red cap)
	1. 4000 rpm 
	2. 5 min 
	3. RT 
3. Take the upper clear phase from the serum or plasma tube. Avoid pipetting any of the red parts. 
4. Pipette serum or plasma in a new eppi. Place eppi on ice. 
5. Place eppis in -70 C freezer




