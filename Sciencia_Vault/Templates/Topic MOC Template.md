---
date_created: <% tp.file.creation_date() %>
status: 
summary: 
tags:
  - MOC
projects:
---
[[Dashboard]]
%% [[Topic MOC Template]] %% 

--- 

_This MOC is meant to encompass a topic of interst for your work. An example could be "Fracture Non-Unions MOC". This acts as a hub for important information relevant to that topic. It's meant more as a drafting hub of ideas for what you need to know to understand the topic as well._

# Overview 

```ad-summary
title: tldr
collapse: open


```

<br> 

```ad-example
title: Topic Overview
collapse: open


```

<br>

```ad-missing
title: Gaps in the field
collapse: open


```

<br>

```ad-seealso
title: Linked Topics
collapse: open


```

<br> 
<br> 

---

# Papers
%% This section is for papers that are directly linked to the topic. This also helps to link the ideas linked to those papers to this topic MOC. %% 

```dataview
TABLE short_title as Title, authors AS "Authors", year AS "Year", summary AS "Summary", URL
FROM "Reference Notes" 
WHERE contains(file.outlinks, [[]]) 
SORT file.cday DESC
```


