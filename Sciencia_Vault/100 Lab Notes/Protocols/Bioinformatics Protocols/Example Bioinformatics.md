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
  - "[[Albert Einstein]]"
source: Source
projects:
  - "[[Example Project MOC]]"
protocol_type: Bioinformatics
---

[[Protocol MOC]]/ [[Ph.D. Dashboard]] 

---


```ad-abstract
title: Purpose

_What is the purpose of this protocol?_


```

---

# Experiments  
_The query will pull any projects that have used this protocol. Sorted by the last modified time of that experiment file._

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
_This query will pull any lab inventory items that are associated with this protocol. Sorted by the last modified time of that experiment file._
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
_Documentation of the actual protocol._




