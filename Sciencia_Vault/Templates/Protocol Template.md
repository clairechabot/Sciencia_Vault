---
created: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - protocol
summary: 
Recommended_by:
source: 
projects: 
protocol_type:
---

[[Protocol MOC]]/ [[Dashboard]] 

---


```ad-abstract
title: Purpose

_Write why this protocol is necessary done and what kind of projects it helps support._ 

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

_Hyperlink any papers from your Zotero catalogue that are relevant to this protocol here._

<br> 




<br> 

---

# Protocol

_Area to document the actual protocol._





