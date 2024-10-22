---
title: "Denormalization in Databases - GeeksforGeeks"
source: "https://www.geeksforgeeks.org/denormalization-in-databases/"
author:
  - "[[GeeksforGeeks]]"
  - "[[https://www.facebook.com/geeksforgeeks.org/]]"
  - "[[https://twitter.com/geeksforgeeks]]"
  - "[[https://www.linkedin.com/company/1299009]]"
  - "[[https://www.youtube.com/geeksforgeeksvideos/]]"
published: 2018-02-18 08:01:35, https://www.facebook.com/geeksforgeeks.org/, https://twitter.com/geeksforgeeks, https://www.linkedin.com/company/1299009, https://www.youtube.com/geeksforgeeksvideos/
created: 2024-10-22
description: "A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions."
tags:
  - "clippings"
---
Last Updated : 30 Sep, 2024

Denormalization is used to alter the structure of a database. Denormalization focuses on adding redundancy which means combining multiple tables so that execute queries quickly. In this article, we’ll explore Denormalization and how it impacts database design.

## What is Denormalization in Databases?

Denormalization is a database optimization technique in which we add redundant data to one or more tables. This can help us avoid costly joins in a relational database. Note that **denormalization** does not mean ‘reversing normalization’ or ‘not to normalize’. It is an optimization technique that is applied after normalization.

Basically, The process of taking a normalized schema and making it non-normalized is called denormalization, and designers use it to tune the performance of systems to support time-critical operations.

In a traditional normalized database, we store data in separate logical tables and attempt to minimize redundant data. We may strive to have only one copy of each piece of data in a database.

For example, in a normalized database, we might have a Courses table and a Teachers table. Each entry in Courses would store the teacherID for a Course but not the teacherName. When we need to retrieve a list of all Courses with the Teacher’s name, we would do a join between these two tables. 

In some ways, this is great; if a teacher changes his or her name, we only have to update the name in one place.   
The drawback is that if tables are large, we may spend an unnecessarily long time doing joins on tables.   
Denormalization, then, strikes a different compromise. Under denormalization, we decide that we’re okay with some redundancy and some extra effort to update the database in order to get the efficiency advantages of fewer joins. 

## What is a Database ?

A database is an organized collection of data or information that’s why it is also known as structured data. Generally database is controlled by a [database management system (DBMS)](https://www.geeksforgeeks.org/introduction-of-dbms-database-management-system-set-1/) because by using DBMS you can easily accessed, managed and updated the data in databases.

There are many types of database :

- No-SQL databases
- Relational databases
- In-memory databases
- Distributed Databases
- Data Warehouses
- Cloud databases

## How is Denormalization Different From Normalization ?

[Normalization](https://www.geeksforgeeks.org/introduction-of-database-normalization/) and [Denormalization](https://www.geeksforgeeks.org/denormalization-in-databases/) both are the method which use in database but it works opposite to each other. One side normalization is used for reduce or removing the redundancy which means there will be no duplicate data or entries in the same table and also optimizes for data integrity and efficient storage, while Denormalization is used for add the redundancy into normalized table so that enhance the functionality and minimize the running time of database queries (like [joins operation](https://www.geeksforgeeks.org/joins-in-dbms/) ) and optimizes for performance and query simplicity.

In a system that demands scalability, like that of any major tech company, we almost always use elements of both normalized and denormalized databases.

### Advantages of Denormalization

- ****Improved Query Performance:**** Denormalization can improve query performance by reducing the number of joins required to retrieve data.
- ****Reduced Complexity****: By combining related data into fewer tables, denormalization can simplify the database schema and make it easier to manage.
- ****Easier Maintenance and Updates:**** Denormalization can make it easier to update and maintain the database by reducing the number of tables.
- ****Improved Read Performance:**** Denormalization can improve read performance by making it easier to access data.
- ****Better Scalability:**** Denormalization can improve the scalability of a database system by reducing the number of tables and improving the overall performance.

### Disadvantages of Denormalization

- ****Reduced Data Integrity:**** By adding redundant data, denormalization can reduce data integrity and increase the risk of inconsistencies.
- ****Increased Complexity:**** While denormalization can simplify the [database schema](https://www.geeksforgeeks.org/database-schemas/) in some cases, it can also increase complexity by introducing redundant data.
- ****Increased Storage Requirements:**** By adding redundant data, denormalization can increase storage requirements and increase the cost of maintaining the [database](https://www.geeksforgeeks.org/what-is-database/).
- ****Increased Update and Maintenance Complexity:**** Denormalization can increase the complexity of updating and maintaining the database by introducing redundant data.
- ****Limited Flexibility:**** Denormalization can reduce the flexibility of a database system by introducing redundant data and making it harder to modify the schema.

## Conclusion

Denormalization is the method which is used to add the redundancy so that execute the query quickly. It is used for decrease the number of tables so that execute the query quickly (like joins operation ). Denormalization improve the storage efficiency so that improve the query performance (like when read heavy systems ). Denormalization has many benefits in some situations but it requires management so that avoid data inconsistencies problems.

## Frequently Asked Questions on Denormalization in Databases – FAQs

### ****Why are we use denormalization ?****

> We use denormalization so that we don’t write complex queries because in denormalization, the reduce the number of tables and the number of joins that’s why using denormalization is used to speed up read and simplify the queries.

### ****When should we use denormalization ?****

> Denormalization is used where read performance is more than critical and where the system is read heavy. Their are some common cases such as where reduce the complexity of fetching and where large amounts of data need.

### ****What is the drawback of denormalization and how do you maintain ?****

> The main problem in denormalization is to maintain data consistency . It is very important so we use triggers and stored procedures so that when data is updated in one place then also updated in other place where it has been duplicated and also use caching techniques or tools to avoid data inconsistency.

### ****How is denormalization different from data aggregation ?****

> Denormalization contains duplicating raw and combining tables while data aggregation involves summarizing and calculating result ( example : sum, average, max , min ) to reduce the data .
> 
> Denormalization focuses on data redundancy but aggregation does not focuses on data redundancy, they focuses on reducing the data size.

  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve