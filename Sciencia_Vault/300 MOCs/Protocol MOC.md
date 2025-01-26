---
aliases: []
tags: [MOC, protocol]
mapofcontent: yes
title: Protocol MOC
date_created: 2024-04-27-Saturday
date_modified: 2024-06-13-Thursday
banner: "![[lab.jpeg]]"
banner_y: 0.684
---

 [[Dashboard]]
%% **Template**: [[Protocol Template]]%%

---

```ad-quote

_"All methods go wrong, but some are useful."_ - **George Box**

```

_A dashboard to organize all of your scientific protocols by experimental type and display which projects they are associated with. This is to make retrieval, documenting, and sharing of them much easier. If the protocol was given to me by someone, that will also be noted within its frontmatter and will appear in the dataview callout._

<br> 

_New protocols (once you click on a button) are automatically sorted into their respective folder within "100 Lab Notes/Protocols"._

## Bioinformatics

<br> 

```meta-bind-button
label: New BioInfo Protocol
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Protocol Template.md
    folderPath: 100 Lab Notes/Protocols/Bioinformatics Protocols
    fileName: New BioInfo Protocol
    openNote: true

```

<br> 

```dataview
TABLE source as "Source", projects AS "Projects", summary AS "Summary"
FROM "100 Lab Notes/Protocols/Bioinformatics Protocols"
SORT filename ASC
```

<br> 

---

## Histology

<br> 

```meta-bind-button
label: New Histo Protocol
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Protocol Template.md
    folderPath: 100 Lab Notes/Protocols/Histology Protocols
    fileName: New Histo Protocol
    openNote: true

```

<br> 

```dataview
TABLE source as "Source", projects AS "Projects", summary AS "Summary"
FROM "100 Lab Notes/Protocols/Histology Protocols"
SORT filename ASC
```

<br> 

---

## In Vitro

<br> 

```meta-bind-button
label: New In Vitro Protocol
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Protocol Template.md
    folderPath: 100 Lab Notes/Protocols/In Vitro Protocols
    fileName: New Intro Protocol
    openNote: true

```

<br> 

```dataview
TABLE source as "Source", projects AS "Projects", summary AS "Summary"
FROM "100 Lab Notes/Protocols/In Vitro Protocols"
SORT filename ASC
```

<br> 

--------

## In Vivo

<br> 

```meta-bind-button
label: New In Vivo Protocol
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Protocol Template.md
    folderPath: 100 Lab Notes/Protocols/In Vivo Protocols
    fileName: New In Vivo Protocol
    openNote: true

```

<br> 

```dataview
TABLE source as "Source", projects AS "Projects", summary AS "Summary"
FROM "100 Lab Notes/Protocols/In Vivo Protocols"
SORT filename ASC
```

<br> 

--------

## Mechanics

<br> 

```meta-bind-button
label: New Mechanics Protocol
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: Templates/Protocol Template.md
    folderPath: 100 Lab Notes/Protocols/Mechanics Protocols
    fileName: New Mechanics Protocol
    openNote: true

```

<br> 

```dataview
TABLE source as "Source", projects AS "Projects", summary AS "Summary"
FROM "100 Lab Notes/Protocols/Mechanics Protocols"
SORT filename ASC
```
