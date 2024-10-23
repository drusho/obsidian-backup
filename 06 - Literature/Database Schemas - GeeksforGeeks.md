---
title: Database Schemas - GeeksforGeeks
source: https://www.geeksforgeeks.org/database-schemas/
author: GeeksforGeeks
published: 2023-03-26 07:50:09
description: A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions.
tags:
  - database
  - schemas
  - sql
---
Nowadays data is one of the most important things in the business world, every business captures its customers data to understand their behavior, in the world of the internet, data is growing like crazy, so businesses need more advanced database solutions by which they can maintain the database systems and whenever they need data to solve business problems, they can easily get what data they want without any problem. To fulfill this condition, there is a requirement for the database schema in the picture.

## What is Schema?

- The Skeleton of the database is created by the attributes and this skeleton is named Schema.
- Schema mentions the logical constraints like table, primary key, etc.
- The schema does not represent the data type of the attributes.

![Details of a Customer](https://media.geeksforgeeks.org/wp-content/uploads/20230511010242/schemadrawio.png)

Details of a Customer

![Schema of Customer](https://media.geeksforgeeks.org/wp-content/uploads/20230511011217/schema1drawio.png)

                                            Schema of Customer 

## Database Schema

- A database schema is a ****logical representation of data**** that shows how the data in a database should be stored logically. It shows how the data is organized and the relationship between the tables.
- Database schema contains table, field, views and relation between different keys like [primary key](https://www.geeksforgeeks.org/primary-key-in-dbms/), [foreign key](https://www.geeksforgeeks.org/foreign-key-constraint-in-sql/).
- Data are stored in the form of files which is unstructured in nature which makes accessing the data difficult. Thus to resolve the issue the data are organized in structured way with the help of database schema.
- Database schema provides the organization of data and the relationship between the stored data.
- Database schema defines a set of guidelines that control the database along with that it provides information about the way of accessing and modifying the data.

## Types of Database Schemas

### ****There are 3 types of database schema:****

### ****Physical Database Schema****

- A Physical schema defines, how the data or information is stored physically in the storage systems in the form of files & indices. This is the actual code or syntax needed to create the structure of a database, we can say that when we design a database at a physical level, it’s called physical schema.
- The Database administrator chooses where and how to store the data in the different blocks of storage.

### ****Logical Database Schema****

- A logical database schema defines all the logical constraints that need to be applied to the stored data, and also describes tables, views, entity relationships, and integrity constraints.
- The Logical schema describes how the data is stored in the form of tables & how the attributes of a table are connected.
- Using ****ER modelling**** the relationship between the components of the data is maintained.
- In logical schema different integrity constraints are defined in order to maintain the quality of insertion and update the data.

### ****View Database Schema****

- It is a view level design which is able to define the interaction between end-user and database.
- User is able to interact with the database with the help of the interface without knowing much about the stored mechanism of data in database.

![View Database Schema](https://media.geeksforgeeks.org/wp-content/uploads/20230510221054/Database-schema.jpeg)

Three Layer Schema Design

## Creating Database Schema

For creating a schema, the statement “CREATE SCHEMA” is used in every database. But different databases have different meanings for this. Below we’ll be looking at some statements for creating a database schema in different database systems:

****1\. MySQL:**** In MySQL, we use the “CREATE SCHEMA” statement for creating the database, because, in MySQL CREATE SCHEMA and CREATE DATABASE, both statements are similar.

****2\. SQL Server:**** In SQL Server, we use the “CREATE SCHEMA” statement for creating a new schema.

****3\. Oracle Database:**** In Oracle Database, we use “CREATE USER” for creating a new schema, because in the Oracle database, a schema is already created with each database user. The statement “CREATE SCHEMA” does not create a schema, instead, it populates the schema with tables & views and also allows one to access those objects without needing multiple SQL statements for multiple transactions. 

## Database Schema Designs

There are many ways to structure a database, and we should use the best-suited schema design for creating our database because ineffective schema designs are difficult to manage & consume extra memory and resources.

Schema design mostly depends on the application’s requirements. Here we have some effective schema designs to create our applications, let’s take a look at the schema designs:

1. Flat Model
2. Hierarchical Model
3. Network Model
4. Relational Model
5. Star Schema
6. Snowflake Schema

## ****Flat Model****

A flat model schema is a 2-D array in which every column contains the same type of data/information and the elements with rows are related to each other. It is just like a table or a spreadsheet. This schema is better for small applications that do not contain complex data.

![Flat-model](https://media.geeksforgeeks.org/wp-content/uploads/20231124120758/Flat-model.jpg)

Designing Flat Model

## ****Hierarchical Model****

Data is arranged using parent-child relationships and a tree-like structure in the Hierarchical Database Model. Because each record consists of several children and one parent, it can be used to illustrate one-to-many relationships in diagrams such as organizational charts. Although obvious, it might not be as adaptable in complicated partnerships.

![Hierarchical Model](https://media.geeksforgeeks.org/wp-content/uploads/20200727111632/hierarchical.png)

Designing Hierarchical Model

## ****Network Model****

The network model and the hierarchical model are quite similar with an important difference that is related to data relationships. The network model allows many-to-many relationships whereas hierarchical models allow one-to-many relationships.

![Network Model](https://media.geeksforgeeks.org/wp-content/uploads/20200727113000/network.png)

Designing Network Model

## ****Relational Model****

The relational model is mainly used for relational databases, where the data is stored as relations of the table. This [relational model schema](https://www.geeksforgeeks.org/relational-model-in-dbms/) is better for object-oriented programming.

![Relational model](https://media.geeksforgeeks.org/wp-content/uploads/20230324112519/relational.jpg)

Designing Relational Model

## ****Star Schema****

Star schema is better for storing and analyzing large amounts of data. It has a fact table at its center & multiple dimension tables connected to it just like a star, where the fact table contains the numerical data that run business processes and the dimension table contains data related to dimensions such as product, time, people, etc. or we can say, this table contains the description of the fact table. The star schema allows us to structure the data of [RDBMS](https://www.geeksforgeeks.org/rdbms-full-form/).

![Star Schema](https://media.geeksforgeeks.org/wp-content/uploads/20230324112549/2.jpg)

Designing Star Schema

## ****Snowflake Schema****

Just like star schema, the snowflake schema also has a fact table at its center and multiple dimension tables connected to it, but the main difference in both models is that in snowflake schema – dimension tables are further normalized into multiple related tables. The snowflake schema is used for analyzing large amounts of data.

![Snowflake Schema](https://media.geeksforgeeks.org/wp-content/uploads/20230324112618/3.jpg)

Designing Snowflake Schema

## Difference between Logical and Physical Database Schema

| ****Physical Schema**** | ****Logical Schema**** |
| --- | --- |
| Physical schema describes the way of storage of data in the disk. | Logical schema provides the conceptual view that defines the relationship between the data entities. |
| Having Low level of abstraction. | Having a high level of abstraction. |
| The design of database is independent to any database management system. | The design of a database must work with a specific database management system or hardware platform. |
| Changes in Physical schema effects the logical schema | Any changes made in logical schema have minimal effect in the physical schema |
| Physical schema does not include attributes. | Logical schema includes attributes. |
| Physical schema contains the attributes and their data types. | Logical schema does not contain any attributes or data types. |
| ****Examples:**** Data definition language(DDL), storage structures, indexes. | ****Examples:**** [Entity Relationship diagram](https://www.geeksforgeeks.org/introduction-of-er-model/), Unified Modeling Language, class diagram. |

## Advantages of Database Schema

- ****Providing Consistency of data:**** [Database schema](https://www.geeksforgeeks.org/database-schemas/) ensures the data consistency and prevents the duplicates.
- ****Maintaining Scalability:**** Well designed database schema helps in maintaining addition of new tables in database along with that it helps in handling large amounts of data in growing tables.
- ****Performance Improvement:**** Database schema helps in faster data retrieval which is able to reduce operation time on the database tables.
- ****Easy Maintenance:**** Database schema helps in maintaining the entire database without affecting the rest of the database
- ****Security of Data:**** Database schema helps in storing the sensitive data and allows only authorized access to the database.

## Database Instance

The database schema is defined before the actual database is created, after the database is operational, it is very difficult to modify the schema because the schema represents the fundamental structure of the database. Database instance does not hold any information related to the saved data in database. Therefore database instance represents the data and information that is currently stored in the database at a specific point in time.

![Database Instance](https://media.geeksforgeeks.org/wp-content/uploads/20230511015635/database-instance.png)

Database instance of Customer table at a specific time

## Database schema versus database instance

| Aspect | Database Schema | Database Instance |
| --- | --- | --- |
| Definition | Blueprint or design of the database structure | Actual data stored in the database at a given time |
| Nature | Static (does not change frequently) | Dynamic (changes with every data modification) |
| Represents | Structure (tables, columns, data types, relationships) | State of the data in the database |
| Example | Table definitions, data types, constraints | Actual rows of data in the tables |
| Change Frequency | Changes infrequently (e.g., during schema design changes) | Changes frequently with transactions |

## Conclusion

- The Structure of the database is referred to as the Schema, and it represents logical restrictions like Table and Key, among other things.
- [Three Schema Architecture](https://www.geeksforgeeks.org/introduction-of-3-tier-architecture-in-dbms-set-2/) was developed to prevent the user from direct access to the database.
- Since the information that is saved in the database is subject to frequent change, Instance is a representation of a data at a specific time.

## FAQs

### What is a database schema?

> It is the blueprint or design for the actual database structure such as tables, columns, data types, and relationships.

### What is a database instance?

> A database instance consists of all the data actually stored at any point in time within a database.

### How does a database instance differ from a database schema?

> Schema: A structure comprising definition, static; instance: dynamic, representing the current state of the data.

### Why is a database schema important?

> It ensures the consistency, scalability, performance, maintenance, and security of the data.

### Can the Schema of a Database Change Frequently?

> No, changes in schema are infrequent, and this mostly happens in the processes of structural update or redesign.

Are you a student in Computer Science or an employed professional looking to take up the **GATE 2025 Exam**? Of course, you can get a good score in it but to get the best score our [GATE CS/IT 2025 - Self-Paced Course](https://gfgcdn.com/tu/Q3U/) is available on GeeksforGeeks to help you with its preparation. Get comprehensive coverage of **all topics of GATE**, detailed explanations, and **practice questions** for study. Study at your pace. Flexible and easy-to-follow modules. Do well in GATE to enhance the prospects of your career. Enroll now and let your journey to success begin!

  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve