---
company: 
location: 
country: 
origin: 
title: 
email: 
phone: 
website: 
aliases: 
project: 
birthday: 
Icon: professional
team: 
tags:
  - people
---

[[People MOC]]

---

<br>

picture:: 


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
