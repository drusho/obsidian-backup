[[+Home]] #MOC

```meta-bind-button

```

# People MOC---
company: 
location: 
title: 
email: 
website: 
aliases: 
---
tags:: [[👥 People MOC]]

# [[People MOC]]


## Notes
- 

## Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "Timestamps/Meetings" where contains(file.outlinks, [[]])
SORT file.cday DESC
```
A personal CRM. People Notes are about jotting down notable information about people and linking people back to [[🗣 Meetings MOC]].

These are the different categories of People Notes:
- Work
- Personal
- Creative
- Fictional
- Notable

---
### Templates
- [[Template, People]]

# People
```dataview
table title
from "Extras/People"
sort file.name asc
```