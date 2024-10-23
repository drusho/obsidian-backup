---
title: Types of Database Management Systems - GeeksforGeeks
source: https://www.geeksforgeeks.org/types-of-database-management-systems/
author:
  - "GeeksforGeeks"
published: 2024-06-28 12:54:18
created: 2024-10-22
description: A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions.
tags:
  - database
  - sql
---
A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner. It allows users to create, modify, and query a database, as well as manage the security and access controls for that database.

## What is DBMS?

A [[Introduction of DBMS (Database Management System)]] is a software or technology used to manage data from a database. It allows users to store, modify and retrieve data in an organized way. It also provides security to the database.

## Types of Database Management Systems

### 1\. Hierarchical DBMS

- [[Hierarchical Model in DBMS - GeeksforGeeks]] organizes data in a tree-like structure with parent-child relationships.
- Each parent can have multiple children, but a child can have only one parent.
- Data navigation is done through paths.

**Syntax:**

```
DBD NAME(database_name)SEGM NAME(segment_name)FIELD NAME(field_name), BYTES(bytes), START(start_byte)
```

****Example:****

```
GET /employees/123/projects/456
```

This retrieves project 456 for employee 123.

### 2\. Network DBMS

- [Network DBMS](https://www.geeksforgeeks.org/network-model-in-dbms/) allows more flexible relationships, where a child can have multiple parents.
- Uses a network model with sets and records.
- Data navigation is done through sets.

**Syntax: (Define Record Type)**

```
RECORD NAME IS record_nameCONTAINS field_specifications
```

**Syntax: (Define Set)**

```
SET NAME IS set_nameOWNER IS owner_recordMEMBER IS member_record
```

****Example****

```
FIND owner OF project 456
```

This finds the owner(s) of project 456.

### 3\. Relational DBMS (RDBMS)

- [Relational DBMS](https://www.geeksforgeeks.org/relational-model-in-dbms/) stores data in tables with rows and columns.
- Relationships are established using keys.
- Data access is done using [SQL (Structured Query Language).](https://www.geeksforgeeks.org/structured-query-language/)

**Syntax: (Create Table)**

```
CREATE TABLE table_name (    column1 datatype PRIMARY KEY,    column2 datatype,    ...);
```

**Syntax: (Insert Data)**

```
INSERT INTO table_name (column1, column2, ...)VALUES (value1, value2, ...);
```

**Syntax: (Select Data)**

```
SELECT column1, column2, ...FROM table_nameWHERE condition;
```

****Example:****

```
SELECT * FROM employees WHERE salary > 50000
```

This retrieves all employees with a salary greater than 50000.

### 4\. NoSQL DBMS

- [NoSQL DBMS](https://www.geeksforgeeks.org/introduction-to-nosql/) is designed for handling large volumes of unstructured or [semi-structured data.](https://www.geeksforgeeks.org/what-is-semi-structured-data/)
- Includes document databases, key-value stores, column-family stores, and graph databases.
- Data access varies depending on the specific NoSQL type.

**Syntax: (Insert Document)**

```
db.collection.insertOne(    { key1: "value1", key2: "value2", ... });
```

**Syntax: (Find Document)**

```
db.collection.find(    { key: "value" });
```

****Example:****

```
db.inventory.find( { status: "A" } )
```

This retrieves inventory items with status “A” in MongoDB.

### 5\. Object Oriented DBMS (ODBMS)

- [Object Oriented DBMS](https://www.geeksforgeeks.org/definition-and-overview-of-odbms/) stores data as objects, which can have attributes and methods.
- Supports [inheritance](https://www.geeksforgeeks.org/inheritance-in-c/), [encapsulation](https://www.geeksforgeeks.org/encapsulation-in-cpp/), and [polymorphism](https://www.geeksforgeeks.org/cpp-polymorphism/).
- Data access is done using object query language (OQL).

**Syntax: (Store Object)**

```
ObjectContainer db = Db4o.openFile("database.db4o");db.store(new Person("John", 30));db.close();
```

Syntax: (Retrieve Object)

```
ObjectContainer db = Db4o.openFile("database.db4o");ObjectSet result = db.queryByExample(new Person(null, 0));while(result.hasNext()) {    Person p = (Person)result.next();    System.out.println(p);}db.close();
```

****Example:****

```
SELECT e.name FROM employees e WHERE e.age > 30
```

This retrieves the names of employees older than 30.

### 6\. Graph-based DBMS

- [Graph-based DBMS](https://www.geeksforgeeks.org/what-is-graph-database/) stores data in graph structures with nodes (entities) and edges (relationships).
- Uses graph query languages like Gremlin or SPARQL.

**Syntax: (Create Node)**

```
CREATE (n:Person {name: 'Alice', age: 30});
```

**Syntax: (Create Relationship)**

```
MATCH (a:Person {name: 'Alice'}), (b:Person {name: 'Bob'})CREATE (a)-[:FRIEND]->(b);
```

**Syntax: (Query Nodes and Relationships)**

```
MATCH (a:Person)-[:FRIEND]->(b:Person)RETURN a, b;
```

****Example:****

```
g.V().has('name', 'Alice').out('knows').values('name')
```

This retrieves the names of people Alice knows.

### 7\. Document Database

- [Document Database](https://www.geeksforgeeks.org/document-databases-in-nosql/) stores data in flexible, semi-structured documents (e.g., JSON, XML, BSON).
- No predefined schema, allowing for [dynamic data structures](https://www.geeksforgeeks.org/static-data-structure-vs-dynamic-data-structure/).
- Data access is done using query languages specific to the document database (e.g., [MongoDB Query Language](https://www.geeksforgeeks.org/what-is-a-mongodb-query/)).

**Syntax: (Insert Document)**

```
db.collection.insertOne(    { name: "John", age: 30, department: "HR" });
```

Syntax: (Query Document)

```
db.collection.find(    { name: "John" });
```

****Example:****

```
db.collection.find({field: "value"})
```

This retrieves documents from a collection where a specific field matches the given value.

### 8\. Centralized Database

- [Centralized Database](https://www.geeksforgeeks.org/difference-between-centralized-database-and-distributed-database/) is used to stored data in a single, central location.
- Easier to manage and maintain data consistency.
- Can become a single point of failure if the central system fails.

### Distributed Database

- [Distribute Database](https://www.geeksforgeeks.org/distributed-database-system/) is used to store data which is distributed across multiple physical locations.
- Improved performance, scalability, and fault tolerance.

## Examples with Outputs

### Example 1: Relational DBMS (MySQL)

#### Create Table and Insert Data:

```
CREATE TABLE Employees (    ID INT PRIMARY KEY,    Name VARCHAR(50),    Department VARCHAR(50));INSERT INTO Employees (ID, Name, Department)VALUES (1, 'John Doe', 'HR'), (2, 'Jane Smith', 'IT');
```

#### Select Data:

```
SELECT * FROM Employees;
```

****Output:****

![RDBMS](https://media.geeksforgeeks.org/wp-content/uploads/20240602202707/Screenshot-2024-06-02-202635.png)

Relational DBMS (MySQL)

### Example 2: NoSQL DBMS (MongoDB)

#### Insert Document and Find Document:

```
db.users.insertOne(    { _id: 1, name: "Alice", age: 30 });db.users.find(    { name: "Alice" });
```

****Output:****

```
{ "_id": 1, "name": "Alice", "age": 30 }
```

### Example 3: Hierarchical DBMS (IBM IMS)

#### Define Segment and Field

```
DBD NAME(EmployeeDB)SEGM NAME(Employee)FIELD NAME(EmpID), BYTES(4), START(1)FIELD NAME(EmpName), BYTES(30), START(5)FIELD NAME(Dept), BYTES(20), START(35)
```

****Output:**** This defines a database called **EmployeeDB** with a segment **Employee** containing three fields: **EmpID**, **EmpName**, and **Dept**.

## Conclusion

In conclusion, different [types of DBMSs](https://www.geeksforgeeks.org/types-of-databases/) serve different purposes and are suited to various types of applications. It acts as an interface between the database and its users or application programs, provides many operations e.g. creating a database, Storing in the database, updating an existing database, delete from the database. Understanding the specific needs, help to choose the right DBMS for optimal performance and scalability.

## Frequently Asked Questions on Types of DBMS – FAQs

### What are the key factors to consider when choosing a DBMS?

> Key factors include the complexity of data, expected workload, scalability needs, budget, data security requirements, and the specific features offered by different DBMS types.

### What is the difference between SQL and NoSQL databases?

> [SQL databases](https://www.geeksforgeeks.org/what-is-sql/) are structured and use a predefined schema, while NoSQL databases are designed for unstructured or semi-structured data and offer more flexible schemas. SQL databases are well-suited for complex queries and transactions, while NoSQL databases excel at handling large volumes of data and scaling horizontally.

### What are some popular examples of relational DBMSs?

> Popular relational DBMSs include MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server, and SQLite.

### What are some popular examples of NoSQL DBMSs?

> Popular NoSQL DBMSs include MongoDB (document database), [Cassandra](https://www.geeksforgeeks.org/introduction-to-apache-cassandra/) (column-family store), Redis (key-value store), and Neo4j (graph database).

  
  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve