---
title: "Hierarchical Model in DBMS - GeeksforGeeks"
source: "https://www.geeksforgeeks.org/hierarchical-model-in-dbms/"
author:
  - "GeeksforGeeks"
published: 2021-07-01 06:35:05
created:
description: "A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions."
tags:
  - "dbms"
  - "database"
---
Last Updated : 07 Jul, 2021

**Hierarchical Model :**  
This is one of the oldest models in a data model which was developed by IBM, in the 1950s. In a hierarchical model, data are viewed as a collection of tables, or we can say segments that form a hierarchical relation. In this, the data is organized into a tree-like structure where each record consists of one parent record and many children. Even if the segments are connected as a chain-like structure by logical associations, then the instant structure can be a fan structure with multiple branches. We call the illogical associations as directional associations.

In the hierarchical model, segments pointed to by the logical association are called the **child segment** and the other segment is called the **parent segment**. If there is a segment without a parent is then that will be called the **root** and the segment which has no children are called the **leaves**. The main disadvantage of the hierarchical model is that it can have one-to-one and one-to-many relationships between the nodes.

**Applications of hierarchical model :**

- Hierarchical models are generally used as semantic models in practice as many real-world occurrences of events are hierarchical in nature like biological structures, political, or social structures.
- Hierarchical models are also commonly used as physical models because of the inherent hierarchical structure of the disk storage system like tracks, cylinders, etc. There are various examples such as Information Management System (IMS) by IBM, NOMAD by NCSS, etc.

**Example 1:** Consider the below Student database system hierarchical model.

![](https://media.geeksforgeeks.org/wp-content/uploads/20210628203735/gfg-660x293.PNG)

Hierarchical model

In the above-given figure, we have few students and few course-enroll and a course can be assigned to a single student only, but a student can enroll in any number of courses and with this the relationship becomes one-to-many. We can represent the given hierarchical model like the below relational tables:

**FACULTY Table**

| **Name** | **Dep** | **Course-taught** |
| --- | --- | --- |
| John | CSE | CA |
| Jake | CSE | SE |
| Royal | CSE | DBMS |

**STUDENT Table**

| **Name** | **Course-enroll** | **Grade** |
| --- | --- | --- |
| Gami | CA | 2.0 |
| Mary | SE | 3.0 |
| Mayen | SE | 4.0 |

**Example 2:** Consider the below cricket database system hierarchical model scheme.  
 

![](https://media.geeksforgeeks.org/wp-content/uploads/20210629205900/GFFHG-660x294.PNG)

Hierarchical model

Here, in this example, for each player, there are some set of positions (P\_POSITION) he plays, a set of places (P\_PLACE), and also a set of birthdates (P\_BDATE) of the players. In the above figure, each node represents a logical record type and is displayed by a list of its fields. The child node represents a set of records that are connected to each record of the parent type, which is due to a many-to-many relationship is from child to parent. In the above, figure, the root node PLAYER states that for every player there will be a set of positions, a set of places (only one), and a set of birthdates (which is only one). 

**Advantages of the hierarchical model :**

- As the database is based on this architecture the relationships between various layers are logically simple so, it has a very simple hierarchical database structure.
- It has data sharing as all data are held in a common database data and therefore sharing of data becomes practical.
- It offers data security and this model was the first database model that offered data security.
- There’s also data integrity as it is based on the parent-child relationship and also there’s always a link between the parents and the child segments.

**Disadvantages of the hierarchical model :**

- Even though this model is conceptually simple and easy to design at the same time it is quite complex to implement.
- This model also lacks flexibility as the changes in the new tables or segments often yield very complex system management tasks. Here, a deletion of one segment can lead to the involuntary deletion of all segments under it.
- It has no standards as the implementation of this model does not provide any specific standard.
- It is also limited as many of the common relationships do not conform to the 1 to N format as required by the hierarchical model.

  
  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve