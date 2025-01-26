---
aliases: []
tags: [MOC]
title: Meetings MOC
date_created: 2024-03-04-Monday
date_modified: 2024-06-13-Thursday
banner: "![[night before the exam.jpg]]"
banner_y: 0.288
---

[[Dashboard]]

%%**Template:** [[Meeting Template]]%%

---

_Meetings are timestamped events with other people, where information is exchanged and collected. These can also be linked to [[People MOC]]._

<br>

```meta-bind-button
label: New Meeting
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Meeting Template.md
    folderPath: 100 Lab Notes/Meetings
    fileName: ""
    openNote: true
  - type: command
    command: insert-current-date

```

<br>

---

# Upcoming Meetings

_Meetings from "100 Lab Notes/Meetings" with status=planned in their frontmatter will appear here. They are sorted by startdate and in ascending order._

<br>

```dataview
TABLE startdate AS "Date", start_time AS "Start Time", location AS "Location", summary AS "Summary"
FROM "100 Lab Notes/Meetings" and -#MOC
WHERE status = "planned"
SORT startdate ASC, start_time ASC
```

<br>
<br>

---

# Weekly Ph.D. Reports

_This accumulates all the weekly reports I have with my supervisor about progress on my Ph.D. that are tagged with "#weekly". This can be edited to your own means._

<br>

```dataview
TABLE startdate AS "Date", summary AS "Summary"
FROM "100 Lab Notes/Meetings" and -#MOC AND #weekly
WHERE status = "done"
SORT startdate DESC
LIMIT 4
```

<br>
<br>

---

# Completed Meetings

_Any meeting with status=done in the frontmatter will appear here in descending order._

<br>

```dataview
TABLE location AS "Location", summary
FROM "100 Lab Notes/Meetings" and -#MOC
WHERE status = "done"
SORT startdate DESC, start_time DESC
```
