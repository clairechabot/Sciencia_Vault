---
aliases: 
cssclasses:
  - table-wide
  - wide-page
  - cards
  - cards-1-1
tags:
  - MOC
title: People MOC
date_created: 2024-03-04-Monday
date_modified: 2024-06-13-Thursday
---

[[Dashboard]]
%%Template: [[People Professional]]%%

---

>> ```meta-bind-button
>> label: New Person
>> icon: ""
>> hidden: false
>> class: ""
>> tooltip: ""
>> id: ""
>> style: primary
>> actions:
>>   - type: command
>>     command: workspace:new-tab
>>   - type: templaterCreateNote
>>     templateFile: Templates/People Professional.md
>>     folderPath: Files/People
>>     fileName: Name
>>     openNote: true
>> 
>> ```

---

<br>

# People

_I made this to act as a modern phonebook within my vault. Yes, LinkedIn and other options exist, but in case you choose not to use that as your contact database for people you meet, work with, networking, take courses from, etc... this can be a nice alternative. I added the "card" css format in the frontmatter, which looks nicer if you choose to add photos of your contacts. If that is not your prerogative, then simply delete the "cards" and "cards-1-1" in the front matter to get a plain list format._

<br> 

_The different buttons can help you organise people via the organisation / labs they are associated with. Simply change the "company" in the dataview table, the name after the < label >, and add the company in the person's frontmatter for it to appear organised here. If you would like to make more buttons, just copy and paste and add it within the "tabbed" section._

<br>

_People notes, when created with the button and if you want them called out below, are stored under "Files/People"._

<br>

> >```dataview 
> >TABLE picture AS Picture, company AS Company, team as Team, title as Title
> >FROM "Files/People"
> >SORT file.name asc
>>```

