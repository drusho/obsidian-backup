---
title: FANG SQL Interview Question and Answers
date: [[2024-09-22]]
author: Sameen
source type: Blog
source:  Medium
cssclasses:
tags: sql, interview, questions
---
tags:: Literature

# Google

**This problem was asked by Google.**
Assume you are given the below table of measurement values from a sensor for several days. Each measurement can happen several times in a given day. Write a query to output the sum of values for every odd measurement and the sum of values for every even measurement by date.

measurements
column_name type   
measurement_id, integer   
measurement_value, integer   
measurement_time, datetime

**Answer**
![[carbon (1).png]]
**Note**: Using PostgreSQL

---
# Facebook

**This problem was asked by Facebook.**
Assume you are given the below tables on users and user posts. Write a query to get the distribution of the number of posts per user.

users
column_name type   
user_id integer  
date datetime

posts
column_name, type  
post_id, integer  
user_id, integer  
body, string  
date, datetime

**Answer**
![[carbon.png]]