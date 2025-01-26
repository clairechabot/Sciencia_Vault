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


[[09-10-2024 Mechanical Testing Training]]

<br> 

---

# Protocol
%%Documentation of the actual protocol.%%

## Evaluation Algorithm

- Remote_Destktop_List
    - Whenever you work on one of the remote computers you need to put an "X" (active on it, take it off when you're done)
    - What I will work with is the "Imaging Workstation"
        - could work for analyzing in vivo scans
        - I've been added on Teams
    - Jan sent me the wiki page on how to get there on my computer
- I'll get my own virtual machine to work off of
- To access the computer
    - type the IP address into the "computer"
    - Username: AO / Center / User that you use below the "Imaging workstation"
    - Password: U(#of the user).2024
- Storage
    - "P:" --> vol_silo
        - store the stuff here
        - once you're done every 2-3 months, move the data to the I drive
        - "MeNU" folder for me --> "Testing Fixators" --> where the last test was
            - "Evluation_testing" --> algorithm used for the system
                - Takes you to MatLab to run the script
                - Need to have an excel open in parallel
                    - MeNU --> "All Files" --> the raw files are the ones I want to open in excel --> "deliminted" --> separate based on semicolon (make sure to click)
- Files
    - Compression load --> starts at the baseline we set it at; what the fixator is experiencing compression wise
    - "Evaluation_test.m*" --> script for the computer program
        - Need to make the MatLab variable
            - Workspace --> new --> give it a name "Test_scenario=Example;"
            - Gives you 3 columns
            - Click the name you gave it --> past the three columns of values you got from the raw measurements
                - First column --> displacement measurements
                - Second column --> load
                - Third column --> time
        - Go to "Editor Tab" --> press the big "Run" button --> gives you the course of the experiment
- Graph
    - Want to see the relationship between the displacement and force measurements
        - analyze in respect for each other
    - Click around 0 displacmeent and then click around 0.06 microns for the displacmenet measurement
        - Gives you new graph (Force x Displacement) --> nicely linear --> gives you the value of teh linear agression (best fit line) --> slope of this curve is interpreeted as stiffness (# * D) --> N / mm
    - Make sure to take a screenshot of both graphs when you do a test
- When you go for a new test, you write in a new varaible name, then in the workspace make the new name of the next test
- Doesn't save somewhere, that's why you need to take the pictures of the graphs
- Close Matlab when done



