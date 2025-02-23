---
company: Princeton University
location: Princeton, New Jersey
country: United States
origin: Germany
title: Theoretical Physicist
email: albert.einstein@princeton.edu
phone: N/A
website: https://www.alberteinstein.info/
aliases: 
  - Einstein
  - Relativity Genius
project: Theory of Relativity
birthday: 1879-03-14
Icon: professional
team: Institute for Advanced Study
tags:
  - people
---

[[People MOC]]

---

<br>

picture:: ![[Albert_einstein.avif|200]]


## Notes
- 


<br> 
<br> 

---

## Papers

```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM 
	"Reference Notes" 
WHERE author=file.name
SORT file.name ASC
```

<br>
<br> 

---

## Projects

```dataview
TABLE file.cday AS Created, summary AS "Summary"
FROM 
	"100 Lab Notes" 
WHERE 
	MOC="yes"
	AND Collaborators=file.name
SORT file.name ASC
```

<br> 
<br> 

---

## Meetings

```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "100 Lab Notes/Meetings" where contains(file.outlinks, [[]])
SORT file.cday DESC
```
