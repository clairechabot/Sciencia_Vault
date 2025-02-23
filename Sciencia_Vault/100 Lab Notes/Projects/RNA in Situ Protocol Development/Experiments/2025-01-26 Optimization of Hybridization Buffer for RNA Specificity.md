---
start_date: 2025-01-26
end_date: 
status: ongoing
id: A06DC545-1F7A-4A43-8429-1A41C70BF7E1
tags:
  - experiment
icon: bacteria_experiment
summary: Testing hybridization buffer conditions for optimal RNA specificity.
project:
  - "[[RNA in Situ High-Throughput Protocol Development]]"
---

# Overview

This experiment aims to optimize the hybridization buffer for RNA in situ hybridization to achieve a higher signal-to-noise ratio. Various buffer compositions will be tested with different formamide concentrations and pH levels.

<br>

## Protocols

- [[RNA Hybridization Protocol]]
- [[Buffer Preparation Protocol]]

<br>

## Collaborators

- [[Albert Einstein]]
- [[Marie Curie]]

<br>

## Lab Inventory

- [[Microplate Reader]]
- [[Pipette Set (Adjustable)]]

<br>

---

# Results 

__The query will pull any tasks with "#result" __ 

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

_Insert a timestamp each day you take a new note._

- Command + shift + P --> current date 
- Command + shift + O --> current time

<br> 

- **2025-01-26**  
    Initial testing of buffer compositions:
    
    - Formamide concentration: 25%, 50%, 75%.
    - pH: 6.5, 7.0, 7.5.
    - Initial results indicate 50% formamide with pH 7.0 provides the best specificity.
- **2025-01-27**  
    Adjusting protocol based on initial results:
    
    - Refining buffer volumes for uniform coverage in microplate reader analysis.

