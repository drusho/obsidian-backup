---
company: 
location: 
title: 
email: 
website: 
aliases: 
---
tags:: [[👥 People MOC]]

# [[<% tp.file.title %>]]
<% await tp.file.move("main_vault/07 - Permanent/People/" + tp.file.title) %>

## Notes
- 

## Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "Timestamps/Meetings" where contains(file.outlinks, [[]])
SORT file.cday DESC
```