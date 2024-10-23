---
title: "Top 45+ SQL Query Interview Questions and Answers (2024)"
source: "https://www.geeksforgeeks.org/sql-query-interview-questions/"
author:
  - "[[GeeksforGeeks]]"
  - "[[https://www.facebook.com/geeksforgeeks.org/]]"
  - "[[https://twitter.com/geeksforgeeks]]"
  - "[[https://www.linkedin.com/company/1299009]]"
  - "[[https://www.youtube.com/geeksforgeeksvideos/]]"
published: 2024-01-08 12:06:43, https://www.facebook.com/geeksforgeeks.org/, https://twitter.com/geeksforgeeks, https://www.linkedin.com/company/1299009, https://www.youtube.com/geeksforgeeksvideos/
created: 2024-10-22
description: "Prepare for your SQL query interviews with confidence! Explore the top 30+ SQL query interview questions and expert answers for 2024. Enhance your skills and ace your SQL interviews effortlessly."
tags: sql, interview, questions
---

****SQL**** or ****Structured Query Language**** is a standard language for relational databases. SQL queries are powerful tools used to, manipulate, and manage data stored in these databases like ****MySQL****, ****Oracle****, ****PostgreSQL****, etc. Whether you’re fetching specific data points, performing complex analyses, or modifying database structures, SQL queries provide a standardized language for executing these tasks efficiently.

Here, we will cover ****45+ MySQL interview questions with answers**** that are commonly asked during ****interviews for Data Analyst**** and ****Data Engineer**** positions at MAANG and other high-paying companies. Whether you are a ****fresher**** or an ****experienced professional**** with ****5****, ****8****, or ****10 years**** of experience, this article gives you all the confidence you need to ace your next interview.

## SQL Query Interview Questions and Answers

We have created three sample tables: Student Table, Program Table, and Scholarship Table. We will be using these tables to perform various query operations.

### ****Student Table****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |
| 203 | Rakesh | Kumar | 5.60 | 2021-09-01 10:00:00 | Biology |
| 204 | Radha | Sharma | 9.20 | 2021-09-01 12:45:00 | Chemistry |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 208 | Navleen | Kaur | 7.00 | 2021-09-01 06:30:00 | Mathematics |

### ****Program Table****

| STUDENT\_REF\_ID | PROGRAM\_NAME | PROGRAM\_START\_DATE |
| --- | --- | --- |
| 201 | Computer Science | 2021-09-01 00:00:00 |
| 202 | Mathematics | 2021-09-01 00:00:00 |
| 208 | Mathematics | 2021-09-01 00:00:00 |
| 205 | Physics | 2021-09-01 00:00:00 |
| 204 | Chemistry | 2021-09-01 00:00:00 |
| 207 | Psychology | 2021-09-01 00:00:00 |
| 206 | History | 2021-09-01 00:00:00 |
| 203 | Biology | 2021-09-01 00:00:00 |

### ****Scholarship Table****

| STUDENT\_REF\_ID | SCHOLARSHIP\_AMOUNT | SCHOLARSHIP\_DATE |
| --- | --- | --- |
| 201 | 5000 | 2021-10-15 00:00:00 |
| 202 | 4500 | 2022-08-18 00:00:00 |
| 203 | 3000 | 2022-01-25 00:00:00 |
| 201 | 4000 | 2021-10-15 00:00:00 |

Let us start by taking a look at some of the ****most asked SQL Query interview questions****:

### 1\. Write a SQL query to fetch “FIRST\_NAME” from the Student table in upper case and use ALIAS name as STUDENT\_NAME.

```
SELECT upper(FIRST_NAME) as STUDENT_NAME from Student;
```

****Output:****

```
SHIVANSH
UMESH
RAKESH
RADHA
KUSH
PREM
PANKAJ
NAVLEEN
```

### 2\. Write a SQL query to fetch unique values of MAJOR Subjects from Student table.

```
SELECT DISTINCT MAJOR from STUDENT; 
or
SELECT MAJOR FROM STUDENT GROUP BY(MAJOR);
```

****Output:****

```
Computer Science
Mathematics
Biology
Chemistry
Physics
History
English
```

### 3\. Write a SQL query to print the first 3 characters of FIRST\_NAME from Student table.

```
SELECT SUBSTRING(FIRST_NAME, 1, 3)  FROM Student;
```

****Output:****

```
Shi
Ume
Rak
Rad
Kus
Pre
Pan
Nav
```

### 4\. Write a SQL query to find the position of alphabet (‘a’) int the first name column ‘Shivansh’ from Student table.

```
SELECT INSTR(FIRST_NAME, 'a') FROM Student WHERE FIRST_NAME = 'Shivansh'; 
```

****Output:****

```
5
```

### 5\. Write a SQL query that fetches the unique values of MAJOR Subjects from Student table and print its length.

```
SELECT MAJOR,LENGTH(MAJOR) FROM Student GROUP BY(MAJOR);                                                         
or                                                                                                                                                                                                                 
SELECT DISTINCT MAJOR, LENGTH(MAJOR) FROM Student;    
```

****Output:****

| MAJOR | LENGTH(MAJOR) |
| --- | --- |
| Computer Science | 16 |
| Mathematics | 11 |
| Biology | 7 |
| Chemistry | 9 |
| Physics | 7 |
| History | 7 |
| English | 7 |

### 6\. Write a SQL query to print FIRST\_NAME from the Student table after replacing ‘a’ with ‘A’.

```
SELECT REPLACE(FIRST_NAME, 'a', 'A') FROM Student;
```

****Output:****

```
ShivAnsh
Umesh
RAkesh
RAdhA
Kush
Prem
PAnkAj
NAvleen
```

### 7\. Write a SQL query to print the FIRST\_NAME and LAST\_NAME from Student table into single column COMPLETE\_NAME.

```
SELECT CONCAT(FIRST_NAME, ' ', LAST_NAME) AS COMPLETE_NAME FROM Student;
```

****Output:****

```
Shivansh Mahajan
Umesh Sharma
Rakesh Kumar
Radha Sharma
Kush Kumar
Prem Chopra
Pankaj Vats
Navleen Kaur
```

### 8\. Write a SQL query to print all Student details from Student table order by FIRST\_NAME Ascending and MAJOR Subject descending .

```
SELECT * FROM Student ORDER BY FIRST_NAME , MAJOR DESC;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 203 | Rakesh | Kumar | 5.6 | 2021-09-01 10:00:00 | Biology |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |

### 9\. Write a SQL query to print details of the Students with the FIRST\_NAME as ‘Prem’ and ‘Shivansh’ from Student table.

```
SELECT * from Student WHERE FIRST_NAME IN ('Prem' , 'Shivansh');
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |

### 10\. Write a SQL query to print details of the Students excluding FIRST\_NAME as ‘Prem’ and ‘Shivansh’ from Student table.

```
SELECT * from Student WHERE FIRST_NAME NOT IN ('Prem', 'Shivansh');
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |
| 203 | Rakesh | Kumar | 5.6 | 2021-09-01 10:00:00 | Biology |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |

### 11\. Write a SQL query to print details of the Students whose FIRST\_NAME ends with ‘a’.

```
SELECT * FROM Student WHERE FIRST_NAME LIKE '%a';
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |

### 12\. Write an SQL query to print details of the Students whose FIRST\_NAME ends with ‘a’ and contains six alphabets.

```
SELECT * FROM Student WHERE FIRST_NAME LIKE '_____a';
```

### 13\. Write an SQL query to print details of the Students whose GPA lies between 9.00 and 9.99.

```
SELECT * FROM Student WHERE GPA BETWEEN 9.00 AND 9.99;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |

### 14\. Write an SQL query to fetch the count of Students having Major Subject ‘Computer Science’.

```
SELECT Major, COUNT(*) as TOTAL_COUNT FROM Student WHERE MAJOR = 'Computer Science';
```

****Output:****

| MAJOR | TOTAL\_COUNT |
| --- | --- |
| Computer Science | 1 |

### 15\. Write an SQL query to fetch Students full names with GPA >= 8.5 and <= 9.5.

```
SELECT CONCAT(FIRST_NAME, ' ', LAST_NAME) AS FULL_NAME FROM Student WHERE GPA BETWEEN 8.5 and 9.5;
```

****Output:****

```
Shivansh Mahajan
Radha Sharma
```

### 16\. Write an SQL query to fetch the no. of Students for each MAJOR subject in the descending order.

```
SELECT MAJOR, COUNT(MAJOR) from Student group by MAJOR order by COUNT(MAJOR) DESC;
```

****Output:****

| MAJOR | COUNT(MAJOR) |
| --- | --- |
| Mathematics | 2 |
| Physics | 1 |
| History | 1 |
| English | 1 |
| Computer Science | 1 |
| Chemistry | 1 |
| Biology | 1 |

### 17\. Display the details of students who have received scholarships, including their names, scholarship amounts, and scholarship dates.

```
SELECT 
    Student.FIRST_NAME,
    Student.LAST_NAME,
    Scholarship.SCHOLARSHIP_AMOUNT,
    Scholarship.SCHOLARSHIP_DATE
FROM 
    Student
INNER JOIN 
    Scholarship ON Student.STUDENT_ID = Scholarship.STUDENT_REF_ID;
```

****Output:****

| FIRST\_NAME | LAST\_NAME | SCHOLARSHIP\_AMOUNT | SCHOLARSHIP\_DATE |
| --- | --- | --- | --- |
| Shivansh | Mahajan | 5000 | 2021-10-15 00:00:00 |
| Umesh | Sharma | 4500 | 2022-08-18 00:00:00 |
| Rakesh | Kumar | 3000 | 2022-01-25 00:00:00 |
| Shivansh | Mahajan | 4000 | 2021-10-15 00:00:00 |

### 18\. Write an SQL query to show only odd rows from Student table.

```
SELECT * FROM Student WHERE student_id % 2 != 0;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |
| 203 | Rakesh | Kumar | 5.6 | 2021-09-01 10:00:00 | Biology |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |

### 19\. Write an SQL query to show only even rows from Student table.

```
SELECT * FROM Student WHERE student_id % 2 = 0;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |

### 20\. List all students and their scholarship amounts if they have received any. If a student has not received a scholarship, display NULL for the scholarship details.

```
SELECT 
    Student.FIRST_NAME,
    Student.LAST_NAME,
    Scholarship.SCHOLARSHIP_AMOUNT,
    Scholarship.SCHOLARSHIP_DATE
FROM 
    Student
LEFT JOIN 
    Scholarship ON Student.STUDENT_ID = Scholarship.STUDENT_REF_ID;
```

### 21\. Write an SQL query to show the top n (say 5) records of Student table order by descending GPA.

```
SELECT * from Student ORDER BY GPA DESC LIMIT 5;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |

### 22\. Write an SQL query to determine the nth (say n=5) highest GPA from a table.

```
SELECT * FROM Student ORDER BY GPA DESC LIMIT 5, 1;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |

![SQL Query Interview Questions and Answers](https://media.geeksforgeeks.org/wp-content/uploads/20231129180134/SQL-Queries-Interview-Questions.webp)

### 23\. Write an SQL query to determine the 5th highest GPA without using LIMIT keyword.

```
SELECT * FROM Student s1 
WHERE 4 = (
    SELECT COUNT(DISTINCT (s2.GPA)) 
    FROM Student s2
    WHERE s2.GPA >= s1.GPA
);
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |

### 24\. Write an SQL query to fetch the list of Students with the same GPA.

```
SELECT s1.* FROM Student s1, Student s2 WHERE s1.GPA = s2.GPA AND s1.Student_id != s2.Student_id;
```

### 25\. Write an SQL query to show the second highest GPA from a Student table using sub-query.

```
SELECT MAX(GPA) FROM Student
WHERE GPA NOT IN(SELECT MAX(GPA) FROM Student);
```

****Output:****

```
9.56
```

### 26\. Write an SQL query to show one row twice in results from a table.

```
SELECT * FROM Student 
UNION ALL
SELECT * FROM Student ORDER BY STUDENT_ID;
```

### 27\. Write an SQL query to list STUDENT\_ID who does not get Scholarship.

```
SELECT STUDENT_ID FROM Student 
WHERE STUDENT_ID NOT IN (SELECT STUDENT_REF_ID FROM Scholarship);
```

****Output:****

```
204
205
206
207
208
```

### 28\. Write an SQL query to fetch the first 50% records from a table.

```
SELECT * 
FROM Student 
LIMIT (SELECT COUNT(*) FROM Student) / 2;
```

### 29\. Write an SQL query to fetch the MAJOR subject that have less than 4 people in it.

```
SELECT MAJOR, COUNT(MAJOR) AS MAJOR_COUNT FROM Student GROUP BY MAJOR HAVING COUNT(MAJOR) < 4;
```

****Output:****

| MAJOR | MAJOR\_COUNT |
| --- | --- |
| Biology | 1 |
| Chemistry | 1 |
| Computer Science | 1 |
| English | 1 |
| History | 1 |
| Mathematics | 2 |
| Physics | 1 |

### 30\. Write an SQL query to show all MAJOR subject along with the number of people in there.

```
SELECT MAJOR, COUNT(MAJOR) AS ALL_MAJOR FROM Student GROUP BY MAJOR;
```

****Output:****

| MAJOR | ALL\_MAJOR |
| --- | --- |
| Biology | 1 |
| Chemistry | 1 |
| Computer Science | 1 |
| English | 1 |
| History | 1 |
| Mathematics | 2 |
| Physics | 1 |

### 31\. Write an SQL query to show the last record from a table.

```
SELECT * FROM Student WHERE STUDENT_ID = (SELECT MAX(STUDENT_ID) FROM STUDENT);
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |

### 32\. Write an SQL query to fetch the first row of a table.

```
SELECT * FROM Student WHERE STUDENT_ID = (SELECT MIN(STUDENT_ID) FROM Student);
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 8.79 | 2021-09-01 09:30:00 | Computer Science |

### 33\. Write an SQL query to fetch the last five records from a table.

```
SELECT * 
FROM (
    SELECT * 
    FROM Student 
    ORDER BY STUDENT_ID DESC 
    LIMIT 5
) AS subquery
ORDER BY STUDENT_ID;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |

### 34\. Write an SQL query to fetch three max GPA from a table using co-related subquery.

```
SELECT DISTINCT GPA FROM Student S1 
WHERE 3 >= (SELECT COUNT(DISTINCT GPA) FROM Student S2 WHERE S1.GPA <= S2.GPA) ORDER BY S1.GPA DESC;
```

****Output:****

```
9.78
9.56
9.2
```

### 35\. Write an SQL query to fetch three min GPA from a table using co-related subquery.

```
SELECT DISTINCT GPA FROM Student S1 
WHERE 3 >= (SELECT COUNT(DISTINCT GPA) FROM Student S2 WHERE S1.GPA >= S2.GPA) ORDER BY S1.GPA;
```

****Output:****

```
5.6
7
7.85
```

### 36\. Write an SQL query to fetch nth max GPA from a table.

```
SELECT DISTINCT GPA FROM Student S1 
WHERE n = (SELECT COUNT(DISTINCT GPA) FROM Student S2 WHERE S1.GPA <= S2.GPA) ORDER BY S1.GPA DESC;
```

### 37\. Write an SQL query to fetch MAJOR subjects along with the max GPA in each of these MAJOR subjects.

```
SELECT MAJOR, MAX(GPA) as MAXGPA FROM Student GROUP BY MAJOR;
```

****Output:****

| MAJOR | MAXGPA |
| --- | --- |
| Biology | 5.6 |
| Chemistry | 9.2 |
| Computer Science | 8.79 |
| English | 9.78 |
| History | 9.56 |
| Mathematics | 8.44 |
| Physics | 7.85 |

### 38\. Write an SQL query to fetch the names of Students who has highest GPA.

```
SELECT FIRST_NAME, GPA FROM Student WHERE GPA = (SELECT MAX(GPA) FROM Student);
```

****Output:****

| FIRST\_NAME | GPA |
| --- | --- |
| Pankaj | 9.78 |

### 39\. Write an SQL query to show the current date and time.

```
Query to get current date : 
SELECT CURDATE();
Query to get current date and time : 
SELECT NOW();
```

### 40\. Write a query to create a new table which consists of data and structure copied from the other table (say Student) or clone the table named Student.

```
CREATE TABLE CloneTable AS SELECT * FROM Student;
```

### 41\. Write an SQL query to update the GPA of all the students in ‘Computer Science’ MAJOR subject to 7.5.

```
UPDATE Student SET GPA = 7.5 WHERE MAJOR = 'Computer Science';
```

Output:

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 7.5 | 2021-09-01 09:30:00 | Computer Science |
| 202 | Umesh | Sharma | 8.44 | 2021-09-01 08:30:00 | Mathematics |
| 203 | Rakesh | Kumar | 5.6 | 2021-09-01 10:00:00 | Biology |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |
| 205 | Kush | Kumar | 7.85 | 2021-09-01 08:30:00 | Physics |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 14:30:00 | English |
| 208 | Navleen | Kaur | 7 | 2021-09-01 06:30:00 | Mathematics |

### 42\. Write an SQL query to find the average GPA for each major.

```
SELECT MAJOR, AVG(GPA) AS AVERAGE_GPA FROM Student GROUP BY MAJOR;
```

****Output:****

| MAJOR | AVERAGE\_GPA |
| --- | --- |
| Biology | 5.6 |
| Chemistry | 9.2 |
| Computer Science | 4 |
| English | 9.78 |
| History | 9.56 |
| Mathematics | 7.72 |
| Physics | 7.85 |

### 43\. Write an SQL query to show the top 3 students with the highest GPA.

```
SELECT * FROM Student ORDER BY GPA DESC LIMIT 3;
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 207 | Pankaj | Vats | 9.78 | 2021-09-01 02:30:00 | English |
| 206 | Prem | Chopra | 9.56 | 2021-09-01 09:24:00 | History |
| 204 | Radha | Sharma | 9.2 | 2021-09-01 12:45:00 | Chemistry |

### 44\. Write an SQL query to find the number of students in each major who have a GPA greater than 7.5.

```
SELECT MAJOR, COUNT(STUDENT_ID) AS HIGH_GPA_COUNT FROM Student WHERE GPA > 3.5 GROUP BY MAJOR;
```

****Output:****

| MAJOR | HIGH\_GPA\_COUNT |
| --- | --- |
| Biology | 1 |
| Chemistry | 1 |
| Computer Science | 1 |
| English | 1 |
| History | 1 |
| Mathematics | 2 |
| Physics | 1 |

### 45\. Write an SQL query to find the students who have the same GPA as ‘Shivansh Mahajan’.

```
SELECT * FROM Student WHERE GPA = (SELECT GPA FROM Student WHERE FIRST_NAME = 'Shivansh' 
AND LAST_NAME = 'Mahajan');
```

****Output:****

| STUDENT\_ID | FIRST\_NAME | LAST\_NAME | GPA | ENROLLMENT\_DATE | MAJOR |
| --- | --- | --- | --- | --- | --- |
| 201 | Shivansh | Mahajan | 4 | 2021-09-01 09:30:00 | Computer Science |

## Conclusion

In summary, mastering SQL query interview questions is essential for anyone looking to excel in roles such as data analysts, data engineers, and business analysts. This guide has provided a comprehensive collection of SQL query interview questions and answers designed to prepare you thoroughly for your interviews.

By understanding and practicing these queries, you can demonstrate your proficiency in SQL, a critical skill that underpins successful data manipulation and analysis in various tech-driven industries.

  
  

[![News](https://media.geeksforgeeks.org/auth-dashboard-uploads/Google-news.svg)](https://news.google.com/publications/CAAqBwgKMLTrzwsw44bnAw?hl=en-IN&gl=IN&ceid=IN%3Aen)

Improve