---
company: University of Paris (Sorbonne)
location: Paris, France
country: France
origin: Poland
title: Physicist and Chemist
email: marie.curie@sorbonne.fr
phone: N/A
website: https://www.curie.fr/
aliases: 
  - Madame Curie
  - Pioneer of Radioactivity
project: Discovery of Polonium and Radium
birthday: 1867-11-07
Icon: professional
team: Curie Laboratory
tags:
  - people
---

[[People MOC]]

---

<br>

picture:: ![[marie_curie.webp|200]]


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
