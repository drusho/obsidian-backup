---
title: "Introduction of DBMS (Database Management System)"
source: "https://www.geeksforgeeks.org/introduction-of-dbms-database-management-system-set-1/"
author:
  - "GeekforGeeks"
published: 2024-09-02
description: "A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions."
tags:
  - "dbms"
  - "databse"
---
Last Updated : 02 Sep, 2024

A ****database**** is a collection of interrelated data that helps in the efficient retrieval, insertion, and deletion of data from the database and organizes the data in the form of tables, views, schemas, reports, etc. ****For Example****, a university database organizes the data about students, faculty, admin staff, etc. which helps in the efficient retrieval, insertion, and deletion of data from it.

## What is DBMS?

A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner. It allows users to create, modify, and query a database, as well as manage the security and access controls for that database. DBMS provides an environment to store and retrieve data in convenient and efficient manner.

### Key Features of DBMS

- **Data modeling:** A DBMS provides tools for creating and modifying data models, which define the structure and relationships of the data in a database.
- **Data storage and retrieval:** A DBMS is responsible for storing and retrieving data from the database, and can provide various methods for searching and querying the data.
- **Concurrency control:** A DBMS provides mechanisms for controlling concurrent access to the database, to ensure that multiple users can access the data without conflicting with each other.
- **Data integrity and security:** A DBMS provides tools for enforcing data integrity and security constraints, such as constraints on the values of data and access controls that restrict who can access the data.
- **Backup and recovery:** A DBMS provides mechanisms for backing up and recovering the data in the event of a system failure.
- **DBMS can be classified into two types:** Relational Database Management System (RDBMS) and Non-Relational Database Management System (NoSQL or Non-SQL)
- **RDBMS:** Data is organized in the form of tables and each table has a set of rows and columns. The data are related to each other through primary and foreign keys.
- **NoSQL:** Data is organized in the form of key-value pairs, documents, graphs, or column-based. These are designed to handle large-scale, high-performance scenarios.

### Types of DBMS

1. **Relational Database Management System (RDBMS):** Data is organized into tables (relations) with rows and columns, and the relationships between the data are managed through primary and foreign keys. SQL (Structured Query Language) is used to query and manipulate the data.
2. **NoSQL DBMS:** Designed for high-performance scenarios and large-scale data, NoSQL databases store data in various non-relational formats such as key-value pairs, documents, graphs, or columns.
3. **Object-Oriented DBMS (OODBMS):** Stores data as objects, similar to those used in object-oriented programming, allowing for complex data representations and relationships

## Database Languages

- **Data Definition Language**
- **Data Manipulation Language**
- **Data Control Language**
- **Transactional Control Language**

## Data Definition Language (DDL)

**DDL** is the short name for Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database.

- **CREATE:** to create a database and its objects like (table, index, views, store procedure, function, and triggers)
- **ALTER:** alters the structure of the existing database
- **DROP:** delete objects from the database
- **TRUNCATE:** remove all records from a table, including all spaces allocated for the records are removed
- **COMMENT:** add comments to the data dictionary
- **RENAME:** rename an object

## Data Manipulation Language (DML)

**DML** is the short name for Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete and update data in a database. **Data query language(DQL)** is the subset of “Data Manipulation Language”. The most common command of DQL is **SELECT** statement. SELECT statement help on retrieving the data from the table without changing anything in the table.

- **SELECT:** retrieve data from a database
- **INSERT:** insert data into a table
- **UPDATE:** updates existing data within a table
- **DELETE:** Delete all records from a database table
- **MERGE:** UPSERT operation (insert or update)
- **CALL:** call a PL/SQL or Java subprogram
- **EXPLAIN PLAN:** interpretation of the data access path
- **LOCK TABLE:** concurrency Control

## Data Control Language (DCL)

**DCL** is short for Data Control Language which acts as an access specifier to the database.(basically to grant and revoke permissions to users in the database

- **GRANT:** grant permissions to the user for running DML(SELECT, INSERT, DELETE,…) commands on the table
- **REVOKE:** revoke permissions to the user for running DML(SELECT, INSERT, DELETE,…) command on the specified table

## Transactional Control Language (TCL)

**TCL** is short for Transactional Control Language which acts as an manager for all types of transactional data and all transactions. Some of the command of TCL are

- **Roll Back:** Used to cancel  or Undo changes made in the database
- **Commit:** It is used to apply or save changes in the database
- **Save Point:** It is used to save the data on the temporary basis in the database

## **Data Query Language (DQL)**

**Data query language(DQL)** is the subset of **“Data Manipulation Language”**. The most common command of DQL is 1the **SELECT statement**. SELECT statement helps us in retrieving the data from the table without changing anything or modifying the table. DQL is very important for retrieval of essential data from a database.

## **Paradigm Shift from File System to DBMS**

 File System manages data using files on a hard disk. Users are allowed to create, delete, and update the files according to their requirements. Let us consider the example of file-based University Management System. Data of students is available to their respective Departments, Academics Section, Result Section, Accounts Section, Hostel Office, etc. Some of the data is common for all sections like Roll No, Name, Father Name, Address, and Phone number of students but some data is available to a particular section only like Hostel allotment number which is a part of the hostel office. Let us discuss the issues with this system:

- **Redundancy of data:** Data is said to be redundant if the same data is copied at many places. If a student wants to change their Phone number, he or she has to get it updated in various sections. Similarly, old records must be deleted from all sections representing that student.
- **Inconsistency of Data:** Data is said to be inconsistent if multiple copies of the same data do not match each other. If the Phone number is different in Accounts Section and Academics Section, it will be inconsistent. Inconsistency may be because of typing errors or not updating all copies of the same data.
- **Difficult Data Access:** A user should know the exact location of the file to access data, so the process is very cumbersome and tedious. If the user wants to search the student hostel allotment number of a student from 10000 unsorted students’ records, how difficult it can be.
- **Unauthorized Access:** File Systems may lead to unauthorized access to data. If a student gets access to a file having his marks, he can change it in an unauthorized way.
- **No Concurrent Access:** The access of the same data by multiple users at the same time is known as concurrency. The file system does not allow concurrency as data can be accessed by only one user at a time.
- **No Backup and Recovery:** The file system does not incorporate any backup and recovery of data if a file is lost or corrupted.

These are the main reasons which made a shift from file system to DBMS. Also See, [Advantages of DBMS over File System](https://www.geeksforgeeks.org/advantages-of-dbms-over-file-system/)

## Advantages of DBMS

- **Data organization:** A DBMS allows for the organization and storage of data in a structured manner, making it easy to retrieve and query the data as needed.
- **Data integrity:** A DBMS provides mechanisms for enforcing data integrity constraints, such as constraints on the values of data and access controls that restrict who can access the data.
- **Concurrent access:** A DBMS provides mechanisms for controlling concurrent access to the database, to ensure that multiple users can access the data without conflicting with each other.
- **Data security:** A DBMS provides tools for managing the security of the data, such as controlling access to the data and encrypting sensitive data.
- **Backup and recovery:** A DBMS provides mechanisms for backing up and recovering the data in the event of a system failure.
- **Data sharing:** A DBMS allows multiple users to access and share the same data, which can be useful in a collaborative work environment.

## Disadvantages of DBMS

- **Complexity:** DBMS can be complex to set up and maintain, requiring specialized knowledge and skills.
- **Performance overhead:** The use of a DBMS can add overhead to the performance of an application, especially in cases where high levels of concurrency are required.
- **Scalability:** The use of a DBMS can limit the scalability of an application, since it requires the use of locking and other synchronization mechanisms to ensure data consistency.
- **Cost:** The cost of purchasing, maintaining and upgrading a DBMS can be high, especially for large or complex systems.
- **Limited Use Cases:** Not all use cases are suitable for a DBMS, some solutions don’t need high reliability, consistency or security and may be better served by other types of data storage.

## Applications of DBMS

- **Enterprise Information:** Sales, accounting, human resources, Manufacturing, online retailers.
- **Banking and Finance Sector:** Banks maintaining the customer details, accounts, loans, banking transactions, credit card transactions. Finance: Storing the information about sales and holdings, purchasing of financial stocks and bonds.
- **University:** Maintaining the information about student course enrolled information, student grades, staff roles.
- **Airlines:** Reservations and schedules.
- **Telecommunications:** Prepaid, postpaid bills maintance.

## Conclusion

A Database Management System (DBMS) is an essential tool for efficiently managing, organizing, and retrieving large volumes of data across various industries. Its ability to handle data securely, ensure integrity, support concurrent access, and provide backup and recovery options makes it indispensable for modern data-driven applications. While DBMSs come with complexities and costs, their benefits in terms of data management and security far outweigh the challenges, making them a crucial component in any data-centric environment

> - [Database Management System – Introduction | Set 2](https://www.geeksforgeeks.org/introduction-of-3-tier-architecture-in-dbms-set-2/)
> - [All DBMS Articles](https://www.geeksforgeeks.org/category/dbms/)
> - [DBMS Quizzes](https://www.geeksforgeeks.org/quiz-corner-gq/)