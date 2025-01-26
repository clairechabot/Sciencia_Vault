---
date_created: 2024-05-27 14:15
status: 
summary: 
tags:
  - excalidraw
  - MOC
excalidraw-open-md: true
excalidraw-plugin: parsed
projects:
  - "[[Example Project MOC]]"
---
[[Ph.D. Dashboard]] 
%% [[Topic MOC Template]] %% 

--- 

```ad-summary
title: tldr
collapse: open

_Summarise what you need to know about the topic in 1-2 sentences._

```

```ad-example
title: Topic Overview

_Overview of essentials regarding the topic._

```


```ad-missing
title: Gaps in the field

_Enter any gaps in the field you may be curious about here._


```


```ad-seealso
title: Linked Topics

_Link other Topoic MOCs here._

```

---

# Papers
_This section is for papers that are directly linked to the topic. This also helps to link the ideas linked to those papers to this topic MOC._ 

```dataview
TABLE short_title as Title, authors AS "Authors", year AS "Year", summary AS "Summary", URL
FROM "Reference Notes" 
WHERE contains(file.outlinks, [[]]) 
```

