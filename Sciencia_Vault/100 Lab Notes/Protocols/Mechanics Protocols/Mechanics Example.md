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
protocol_type: Mechanics
---

[[Protocol MOC]]/ [[Ph.D. Dashboard]] 

---


```ad-abstract
title: Purpose

_Write why this protocol is necessary done and what kind of projects it helps support._ 

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

