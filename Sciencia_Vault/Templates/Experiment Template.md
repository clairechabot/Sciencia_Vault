---
start_date: <% tp.date.now("YYYY-MM-DD") %>
end_date: 
status: ongoing
id: <% tp.user.uuid() %>
tags:
  - experiment
Icon: 
summary: 
project:
---

[[Dashboard]] 

---


```ad-abstract
title: Purpose

_Write why this experiment is being done and how it supports the Project MOC it's linked to._ 

```


# Overview 

_In the front matter:_
- _The "id" provides a unique ID for each experiment, so that they can be organised in a different manner than date. This way, multiple experiments can be made per date without confusing overlap. 
- _Under "project" make sure to link to the appropriate project MOC so it will appear on the dataview callout.
- _Icon --> you can assign different icons to what kind of experiment this is. See screenshot below from the Supercharged Links Plugin settings._

![[Screenshot 2025-01-26 at 14.18.10.png]]


<br> 


## Protocols 

_Link protocols from "100 Lab Notes/Protocols" here that you use for the experiment._

<br> 

## Collaborators 

_I hyperlink people notes here to keep track of who has been working on experiments with me._

<br> 

## Lab Inventory

_Link any lab inventory used from "100 Lab Notes/Lab Inventory" here. When you do, the relevant projects show up on that inventory items page so you can trace where it's been used._

<br> 

---

# Results 
%% The query will pull any tasks with "#result" %% 

 ```dataview
	LIST
	FROM "100 Lab Notes/Projects" 
	WHERE econtains(tags, "#results") AND file.path=this.file.path
	GROUP BY file.link
	SORT file.ctime ASC
```

<br> 

---

# Tasks

<br> 

```dataview 
TASK 
	WHERE 
		file.path = this.file.path 
		AND !completed 
	SORT file.name asc
```

<br> 

---

# Entries 

%%
_Insert a timestamp each day you take a new note._

- Command + shift + P --> current date 
- Command + shift + O --> current time
%%

