---
title: "Joins in DBMS - GeeksforGeeks"
source: "https://www.geeksforgeeks.org/joins-in-dbms/"
author:
  - "[[GeeksforGeeks]]"
  - "[[https://www.facebook.com/geeksforgeeks.org/]]"
  - "[[https://twitter.com/geeksforgeeks]]"
  - "[[https://www.linkedin.com/company/1299009]]"
  - "[[https://www.youtube.com/geeksforgeeksvideos/]]"
published: 2023-10-09 12:15:34, https://www.facebook.com/geeksforgeeks.org/, https://twitter.com/geeksforgeeks, https://www.linkedin.com/company/1299009, https://www.youtube.com/geeksforgeeksvideos/
created: 2024-10-22
description: "A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions."
tags: database, sql, joins
---
A join is an operation that combines the rows of two or more tables based on related columns. This operation is used for retrieving the data from multiple tables simultaneously using common columns of tables. In this article, we are going to discuss every point about joins.

## What is Join?

Join is an operation in [DBMS(Database Management System)](https://www.geeksforgeeks.org/introduction-of-dbms-database-management-system-set-1) that combines the row of two or more tables based on related columns between them. The main purpose of Join is to retrieve the data from multiple tables in other words Join is used to perform multi-table queries. It is denoted by ⨝.

#### Syntax 1

> R3 <- ⨝<sup><span>(R1) </span></sup> <join\_condition> <sup><span>(R2)</span></sup>

where R1 and R2 are two relations to be joined and R3 is a relation that will hold the result of the join operation.

#### Example

> Temp <- ⨝<sup><span>(student)</span></sup> <sub><span> S.roll==E.roll</span></sub><sup><span>(Exam)</span></sup>

where S and E are aliases of the student and exam respectively

## SQL JOIN Example

Consider the two tables below as follows:

![Student](https://media.geeksforgeeks.org/wp-content/uploads/20240528160334/table1-3.png)

Table 1 – Student

![Student Course](https://media.geeksforgeeks.org/wp-content/uploads/20240528160410/table5.png)

Table 2 – StudentCourse

Both these tables are connected by one common key (column) i.e. ROLL\_NO.

We can perform a JOIN operation using the given SQL query:

```
SELECT s.roll_no, s.name, s.address, s.phone, s.age, sc.course_idFROM Student sJOIN StudentCourse sc ON s.roll_no = sc.roll_no;
```

****Output:****

| ROLL\_NO | NAME | ADDRESS | PHONE | AGE | COURSE\_ID |
| --- | --- | --- | --- | --- | --- |
| 1 | HARSH | DELHI | xxxxxxxxxx | 18 | 1 |
| 2 | PRATIK | BIHAR | xxxxxxxxxx | 19 | 2 |
| 3 | PRIYANKA | SILIGURI | xxxxxxxxxx | 20 | 2 |
| 4 | DEEP | RAMNAGAR | xxxxxxxxxx | 18 | 3 |
| 5 | SAPTARHI | KOLKATA | xxxxxxxxxx | 19 | 1 |

## Types of Join

 There are many types of Joins in SQL. Depending on the use case, you can use different types of SQL JOIN clauses. Here are the frequently used SQL JOIN types:

## 1\. Inner Join

[Inner Join](https://www.geeksforgeeks.org/sql-inner-join) is a join operation in DBMS that combines two or more tables based on related columns and returns only rows that have matching values among tables. Inner join of two types.

![Inner Join](https://media.geeksforgeeks.org/wp-content/uploads/20240528163448/6a0120a85dcdae970b012877702708970c-pi.png)

Inner Join

- Conditional join
- Equi Join
- Natural Join

### (a) Conditional Join

Conditional join or Theta join is a type of inner join in which tables are combined based on the specified condition.

In conditional join, the join condition can include <, >, <=, >=, ≠ operators in addition to the = operator.

****Example:**** Suppose two tables A and B

****Table A****

| R | S |
| --- | --- |
| 10 | 5 |
| 7 | 20 |

****Table B****

| T | U |
| --- | --- |
| 10 | 12 |
| 17 | 6 |

> A ⨝ <sub><span>S&lt;T </span></sub> B

****Output****

| R | S | T | U |
| --- | --- | --- | --- |
| 10 | 5 | 10 | 12 |

****SQL Query****

> SELECT R, S, T, U FROM TableA JOIN TableB ON S < T;

****Explanation:**** This query joins the table A, B and projects attributes R, S, T, U were condition S < T is satisfied.

### (b) Equi Join

[Equi Join](https://www.geeksforgeeks.org/sql-equi-join-and-non-equi-join) is a type of Inner join in which we use equivalence(‘=’) condition in the join condition

****Example:**** Suppose there are two tables Table A and Table B

****Table A****

| Column A | Column B |
| --- | --- |
| a | a |
| a | b |

****Table B****

| Column A | Column B |
| --- | --- |
| #### a | #### a |
| #### a | #### c |

> A ⨝ <sub><span> A.Column B = B.Column B</span></sub> (B)

****Output****

| Column A | Column B |
| --- | --- |
| a | a |

****SQL Query****

> SELECT \* FROM TableA NATURAL JOIN TableB;

****Explanation –**** The data value “a” is available in both tables Hence we write that “a” is the table in the given output.

### (b) Natural Join

[Natural join](https://www.geeksforgeeks.org/sql-natural-join) is a type of inner join in which we do not need any comparison operators. In natural join, columns should have the same name and domain. There should be at least one common attribute between the two tables.

****Example:**** Suppose there are two tables Table A and Table B

****Table A****

| Number | Square |
| --- | --- |
| 2 | 4 |
| 3 | 9 |

****Table B****

| Number | Cube |
| --- | --- |
| 2 | 8 |
| 3 | 27 |

> A ⨝ B

****Output****

| Number | Square | Cube |
| --- | --- | --- |
| 2 | 4 | 8 |
| 3 | 9 | 27 |

****SQL Query****

> SELECT \* FROM TableA NATURAL JOIN TableB;

****Explanation –**** Column Number is available in both tables Hence we write the “Number column once ” after combining both tables.

## 2\. Outer Join

[Outer join](https://www.geeksforgeeks.org/sql-outer-join) is a type of join that retrieves matching as well as non-matching records from related tables. These three types of outer join

- Left outer join
- Right outer join
- Full outer join

### (a) Left Outer Join

It is also called [left join](https://www.geeksforgeeks.org/sql-left-join). This type of outer join retrieves all records from the left table and retrieves matching records from the right table.

****Example:**** Suppose there are two tables Table A and Table B

****Table A****

| Number | Square |
| --- | --- |
| 2 | 4 |
| 3 | 9 |
| 4 | 16 |

****Table B****

| Number | Cube |
| --- | --- |
| 2 | 8 |
| 3 | 27 |
| 5 | 125 |

> A ⟕ B

****Output****

| Number | Square | Cube |
| --- | --- | --- |
| 2 | 4 | 8 |
| 3 | 9 | 27 |
| 4 | 16 | NULL |

****SQL Query-****

> ****SELECT \* FROM TableA LEFT OUTER JOIN TableB ON TableA.Number = TableB.Number;****

****Explanation****: Since we know in the left outer join we take all the columns from the left table (Here Table A) In the table A we can see that there is no Cube value for number 4. so we mark this as NULL.

### (b) Right Outer Join

It is also called a [right join](https://www.geeksforgeeks.org/sql-right-join). This type of outer join retrieves all records from the right table and retrieves matching records from the left table. And for the record which doesn’t lies in Left table will be marked as NULL in result Set.

![Right outer join](https://media.geeksforgeeks.org/wp-content/uploads/20240528163604/join-660.jpg)

Right Outer Join

****Example:**** Suppose there are two tables Table A and Table B

> A ⟖ B

****Output:****

| Number | Square | Cube |
| --- | --- | --- |
| 2 | 4 | 8 |
| 3 | 9 | 27 |
| 5 | NULL | 125 |

****SQL Query****

> ****SELECT \* FROM TableA RIGHT OUTER JOIN TableB ON TableA.Number= TableB.Number;****

****Explanation:**** Since we know in the right outer join we take all the columns from the right table (Here Table B) In table A we can see that there is no square value for number 5. So we mark this as NULL.

### (c) Full Outer Join

[****FULL JOIN****](https://www.geeksforgeeks.org/sql-full-join) creates the result set by combining the results of both LEFT JOIN and RIGHT JOIN. The result set will contain all the rows from both tables. For the rows for which there is no matching, the result set will contain **NULL** values.

****Example:**** Table A and Table B are the same as in the left outer join

> A ⟗ B

****Output:****

| Number | Square | Cube |
| --- | --- | --- |
| 2 | 4 | 8 |
| 3 | 9 | 27 |
| 4 | 16 | NULL |
| 5 | NULL | 125 |

****SQL Query****

> ****SELECT \* FROM TableA FULL OUTER JOIN TableB ON TableA.Number= TableB.Number;****

Explanation: Since we know in full outer join we take all the columns from both tables (Here Table A and Table B) In the table A and Table B we can see that there is no Cube value for number 4 and No Square value for 5 so we mark this as NULL.

## Conclusion

In the field of Database Management Systems, Join is a very important tool for retrieving data from multiple tables simultaneously. Learning and understanding join syntax and types of syntax including inner and outer joins is very efficient for writing queries for databases and extracting valuable understanding.

## Frequently Asked Questions on Joins – FAQs

### ****What is the primary purpose of a join operation in DBMS?****

> The Primary purpose of join operation in DBMS is to join two or more tables based on related columns , enabling the retrieval of data from multiple tables in single query.

### ****What is the difference between an inner join and an outer join?****

> An inner join returns the only matching values that available in both tables while outer join returns all the data which is matching as well as non-matching values from the both tables.

### ****When is an Equi Join used in a database query?****

> An Equi Join is a type of inner join that uses equivalence (usually ‘=’) conditions in the join condition. It is used when you want to combine rows where specific columns have equal values****.****

### ****What is a Natural Join, and when is it used?****

> A Natural Join is a type of inner join where no comparison operators are needed. It is used when columns in the two tables have the same name and domain, and there is at least one common attribute between them.

### ****In a full outer join, what does the result table include?****

> In a full outer join, the result table includes all the rows from both tables, whether they have matching values or not.

  
  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve