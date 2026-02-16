# 📘 Database Management System (DBMS) — Full Notes  
**Author:** Abdul Muqsit  

---

## 📑 Table of Contents  

- [1. What is DBMS?](#1-what-is-dbms)  
- [2. Data Models in DBMS](#2-data-models-in-dbms)  
- [3. Advantages of DBMS](#3-advantages-of-dbms)  
- [4. DBMS vs RDBMS](#4-dbms-vs-rdbms)  
- [5. Table, Rows, Columns](#5-table-rows-columns)  
- [6. Components of DBMS](#6-components-of-dbms)  
- [7. Primary, Candidate & Foreign Keys](#7-primary-candidate--foreign-keys)  
- [8. Primary Key vs Unique Key](#8-primary-key-vs-unique-key)  
- [9. Normalization](#9-normalization)  
- [10. Denormalization](#10-denormalization)  
- [11. Schema](#11-schema)  
- [12. ER Diagram](#12-er-diagram)  
- [13. Relationships in DBMS](#13-relationships-in-dbms)  
- [14. Constraints](#14-constraints)  
- [15. OLTP vs OLAP](#15-oltp-vs-olap)  
- [16. Delete vs Truncate](#16-delete-vs-truncate)  
- [17. Role of DBA](#17-role-of-dba)  
- [18. Joins in SQL](#18-joins-in-sql)  
- [19. Subqueries](#19-subqueries)  
- [20. Aggregate Functions](#20-aggregate-functions)  
- [21. UNION vs UNION ALL](#21-union-vs-union-all)  
- [22. Transactions](#22-transactions)  
- [23. ACID Properties](#23-acid-properties)  
- [24. Data Redundancy](#24-data-redundancy)  
- [25. Deadlock](#25-deadlock)  
- [26. Concurrency Control & Locking](#26-concurrency-control--locking)  
- [27. Commit & Rollback](#27-commit--rollback)  
- [28. Triggers](#28-triggers)  
- [29. Superkey vs Candidate Key](#29-superkey-vs-candidate-key)  
- [30. GROUP BY](#30-group-by)  
- [31. Trigger vs Stored Procedure](#31-trigger-vs-stored-procedure)  
- [32. Data Partitioning](#32-data-partitioning)  
- [33. Views](#33-views)  
- [34. Types of DBMS](#34-types-of-dbms)  
- [35. Conflict Serializability](#35-conflict-serializability)  
- [36. SQL Window Functions](#36-sql-window-functions)  
- [37. Indexes in DBMS](#37-indexes-in-dbms)  
- [38. Distributed Databases](#38-distributed-databases)  
- [39. NoSQL Databases Basics](#39-nosql-databases-basics)  

---

## 🟦 1. What is DBMS?
A **Database Management System (DBMS)** is software used to **store, manage, and retrieve** data efficiently.  
It provides an interface between users and the database.


---

## 🟦 2. Data Models in DBMS
Data models define how data is logically structured.

- **Hierarchical Model:** Data organized in a tree-like structure.  
- **Network Model:** Multiple parent-child relationships (graph-based).  
- **Relational Model:** Data stored in tables (relations).  
- **Object-Oriented Model:** Data represented as objects.


---

## 🟦 3. Advantages of DBMS
- Data Integrity and Security  
- Efficient Data Retrieval  
- Reduced Redundancy  
- Backup & Recovery Mechanisms  
- Multi-user Concurrent Access  
- Easy Data Sharing  

---

## 🟦 4. DBMS vs RDBMS

| DBMS                          |              RDBMS           |
|-------------------------------|------------------------------|
| No relations between data     | Tables have relationships    |
| No constraints                | Supports primary/foreign keys|
| Unstructured data             | Structured schema            |
| Examples: XML DB, File System | MySQL, SQL Server, Oracle    |


---

## 🟦 5. Table, Rows, Columns

| ID | Name  | Age |
|----|-------|-----|
| 1  | Alice | 23  |  
| 2  | Bob   | 25  | 

- **Table:** Collection of rows and columns.  
- **Row (Tuple):** A single record entry.  
- **Column (Attribute):** A property of data entity.

---

## 🟦 6. Components of DBMS
- Database Engine  
- Query Processor  
- Transaction Manager  
- Storage Manager  
- Metadata/Schema Manager  

---

## 🟦 7. Primary, Candidate & Foreign Keys

|        Students               |              |       Departments         |
|-------------------------------|--------------|---------------------------|
| StudentID |  Name  | DeptID   |     -->      |  DeptID  |   DeptName     |
|-----------|--------|----------|--------------|----------|----------------|
|    101    |  Alice |   D01    |              |   D0     |      CS        |
|    102    |  Bob   |   D02    |              |   D02    |      EE        |


                          
- **Primary Key:** Uniquely identifies a record.  
- **Candidate Key:** All fields that could be primary keys.  
- **Foreign Key:** Links data between tables.

---

## 🟦 8. Primary Key vs Unique Key
- Both enforce **uniqueness**.  
- **Unique Key** allows `NULL`; **Primary Key** doesn’t.

---

## 🟦 9. Normalization
Process of organizing data to reduce redundancy.

| Type  |      Rule                           |
|-------|-------------------------------------|
| 1NF   | Atomic values only                  |
| 2NF   | No partial dependency               |
| 3NF   | No transitive dependency            |
| BCNF  | All determinants are candidate keys |

---

## 🟦 10. Denormalization
Combining related tables to **improve performance** in read-heavy systems.

---

## 🟦 11. Schema
A **logical blueprint** of the entire database — defines structure, views, relationships.

---

## 🟦 12. ER Diagram
Shows entities, their attributes, and relationships.

**Example:**  
![ER Diagram](<img width="254" height="199" alt="image" src="https://github.com/user-attachments/assets/142c61b6-3ddc-453a-8841-d7637c2330f4" />)

---

## 🟦 13. Relationships in DBMS
- **One-to-One (1:1)**  
- **One-to-Many (1:M)**  
- **Many-to-Many (M:N)**

---

## 🟦 14. Constraints
- `NOT NULL`  
- `UNIQUE`  
- `PRIMARY KEY`  
- `FOREIGN KEY`  
- `CHECK`  
- `DEFAULT`

---

## 🟦 15. OLTP vs OLAP

| Feature | OLTP | OLAP |
|----------|------|------|
| Purpose | Real-time data processing | Analytical processing |
| Example | ATM, Banking system | Data warehouse |
| Speed | Fast | Handles massive data slowly |

---

## 🟦 16. Delete vs Truncate
- **DELETE:** Removes selected rows; can be rolled back.  
- **TRUNCATE:** Deletes all rows; faster; cannot roll back.

---

## 🟦 17. Role of DBA
- Database design & modeling  
- Backups & recovery  
- Performance tuning  
- Security management  
- Troubleshooting  

---

## 🟦 18. Joins in SQL
**Types:** `INNER`, `LEFT`, `RIGHT`, `FULL`, `CROSS`, `SELF`

SELECT S.Name, D.DeptName
FROM Students S
INNER JOIN Departments D
ON S.DeptID = D.DeptID;


**Output:**

| Name  | DeptName |
|------ |----------|
| Alice |    CS    |
| Bob   |    EE    |

---

## 🟦 19. Subqueries
A **query inside another query**.

SELECT Name
FROM Students
WHERE DeptID = (
SELECT DeptID FROM Departments WHERE DeptName='CS'
);

text

---

## 🟦 20. Aggregate Functions
Common functions: `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`

SELECT DeptID, AVG(Salary) AS AvgSalary
FROM Employees
GROUP BY DeptID;

text

---

## 🟦 21. UNION vs UNION ALL

|   Feature  |         UNION          |           UNION ALL               |
|------------|------------------------|-----------------------------------|
| Duplicates | Removed                | Included                          |
| Performance| Slower (deduplication) | Faster (no deduplication)         |
| Use Case   | Unique records         | All records, including duplicates |

**Example:**

SELECT Name FROM Table1
UNION
SELECT Name FROM Table2;

SELECT Name FROM Table1
UNION ALL
SELECT Name FROM Table2;

text

- **UNION:** Returns only unique names from both tables.  
- **UNION ALL:** Returns all names, including duplicates.

---

## 🟦 22. Transactions
A group of SQL operations executed together as one logical unit.  
**Example:** Bank transfer – Debit + Credit + Commit.

---

## 🟦 23. ACID Properties
- **Atomicity** → All or none  
- **Consistency** → Valid states only  
- **Isolation** → Each transaction independent  
- **Durability** → Changes permanent after commit  

---

## 🟦 24. Data Redundancy
Repetition of data; wastes storage.  
**Solution:** Use normalization.

---

## 🟦 25. Deadlock
Two transactions wait indefinitely for each other’s locked resources.

---

## 🟦 26. Concurrency Control & Locking
- **Shared Lock:** For read operations.  
- **Exclusive Lock:** For write operations.

---

## 🟦 27. Commit & Rollback
- **COMMIT:** Save all changes permanently.  
- **ROLLBACK:** Undo recent uncommitted changes.

---

## 🟦 28. Triggers
Automatic execution of procedures when database events occur (INSERT, UPDATE, DELETE).

---

## 🟦 29. Superkey vs Candidate Key
- **Superkey:** May include extra attributes.  
- **Candidate Key:** Minimal superkey.

---

## 🟦 30. GROUP BY
Used to group identical data.

SELECT DeptID, COUNT(*)
FROM Employees
GROUP BY DeptID;

text

---

## 🟦 31. Trigger vs Stored Procedure

| Trigger | Stored Procedure |
|----------|------------------|
| Executes automatically | Executes manually |
| Cannot accept parameters | Can accept parameters |

---

## 🟦 32. Data Partitioning
- **Horizontal Partition:** Divide rows.  
- **Vertical Partition:** Divide columns.  
- **Range/Hash Partition:** Based on values or hash keys.

---

## 🟦 33. Views
A **virtual table** created from a query.

CREATE VIEW emp_view AS
SELECT Name, Salary FROM Employees WHERE Salary > 5000;

text

---

## 🟦 34. Types of DBMS
- Hierarchical  
- Network  
- Relational  
- Object-Oriented  

---

## 🟦 35. Conflict Serializability
If no cycle exists in the **precedence graph**, schedule is **conflict-serializable**.

---

## 🟦 36. SQL Window Functions
Perform calculations across sets of rows related to the current row.

SELECT Name, Salary,
AVG(Salary) OVER (PARTITION BY DeptID) AS AvgDeptSalary
FROM Employees;

text

---

## 🟦 37. Indexes in DBMS
Indexes improve query performance.

|      Type     |      Description         |           Example                               |
|---------------|--------------------------|-------------------------------------------------|
| Single-column | Index on one column      | `CREATE INDEX idx_name ON Students(Name);`      |
| Composite     | Index on multiple columns| `CREATE INDEX idx_multi ON Students(Name, Age);`|
| Clustered     | Reorders data physically |  Default on primary key                         |
| Non-Clustered | Separate structure       |  Secondary lookup                               |

     
---

## 🟦 38. Distributed Databases
Databases distributed across multiple physical locations.

**Advantages:** Scalability, fault tolerance, faster local access.  
**Challenges:** Synchronization, replication delay.

---

## 🟦 39. NoSQL Databases Basics
Used for **unstructured** or **semi-structured** data.

**Types:**  
- Key-Value (Redis)  
- Document (MongoDB)  
- Column (Cassandra)  
- Graph (Neo4j)

**Example:** MongoDB stores data as JSON-like documents `{ "_id":1, "name":"Alice" }`

---

## 🟦 40. Row Functions (Interview-Focused)

Row functions operate on **individual rows** and return a value for each row. These are commonly asked in interviews.

---

### ✅ **1. ROW_NUMBER()**

Assigns a unique sequential number to each row **within a partition**, based on a specified order.

**Example:**

```sql
SELECT Name, Salary,
ROW_NUMBER() OVER (ORDER BY Salary DESC) AS RankBySalary
FROM Employees;
```

| Name  | Salary | RankBySalary |
| ----- | ------ | ------------ |
| Ali   | 90000  | 1            |
| Rahul | 85000  | 2            |
| Sneha | 80000  | 3            |

**Use Case:** Find top-N, remove duplicates.

---

### ✅ **2. RANK()**

Assigns rank but **skips numbers** when duplicates appear.

**Example:**

```sql
SELECT Name, Salary,
RANK() OVER (ORDER BY Salary DESC) AS SalaryRank
FROM Employees;
```

| Name  | Salary | Rank |
| ----- | ------ | ---- |
| Ali   | 90000  | 1    |
| Rahul | 85000  | 2    |
| Riya  | 85000  | 2    |
| Sneha | 80000  | 4    |

---

### ✅ **3. DENSE_RANK()**

Similar to `RANK()` but **does not skip numbers**.

**Example:**

```sql
SELECT Name, Salary,
DENSE_RANK() OVER (ORDER BY Salary DESC) AS DenseRank
FROM Employees;
```

| Name  | Salary | DenseRank |
| ----- | ------ | --------- |
| Ali   | 90000  | 1         |
| Rahul | 85000  | 2         |
| Riya  | 85000  | 2         |
| Sneha | 80000  | 3         |

---

### ✅ **4. NTILE(n)**

Divides rows into **n equal groups**.

**Example:**

```sql
SELECT Name, Salary,
NTILE(4) OVER (ORDER BY Salary DESC) AS QuartileGroup
FROM Employees;
```

| Name  | Salary | QuartileGroup |
| ----- | ------ | ------------- |
| Ali   | 90000  | 1             |
| Rahul | 85000  | 1             |
| Sneha | 80000  | 2             |
| Riya  | 78000  | 2             |
| John  | 62000  | 3             |
| Aman  | 50000  | 4             |

---

### ✅ **5. LAG()** (Previous Row Value)

Fetches value from **previous row**.

**Example:**

```sql
SELECT Name, Salary,
LAG(Salary, 1, 0) OVER (ORDER BY Salary DESC) AS PreviousSalary
FROM Employees;
```

---

### ✅ **6. LEAD()** (Next Row Value)

Fetches value from **next row**.

**Example:**

```sql
SELECT Name, Salary,
LEAD(Salary, 1, 0) OVER (ORDER BY Salary DESC) AS NextSalary
FROM Employees;
```

---

### 📝 **Interview Tips (Very Useful!)**

* **ROW_NUMBER()** → remove duplicates, pagination.
* **RANK()**       → competitions where equal scores share rank.
* **DENSE_RANK()** → similar but ranks are continuous.
* **NTILE()**      → percentile, quartile grouping.
* **LAG()/LEAD()** → trend analysis (salary change, stock price change).

---

-- 🟦 41. Common Salary Queries (Interview-Focused)
```sql

-- 1. Highest Salary
SELECT MAX(Salary) AS HighestSalary
FROM Employees;

-- 2. Lowest Salary
SELECT MIN(Salary) AS LowestSalary
FROM Employees;

-- 3. Second Highest Salary

-- Option 1: Using Subquery
SELECT MAX(Salary) AS SecondHighestSalary
FROM Employees
WHERE Salary < (SELECT MAX(Salary) FROM Employees);

-- Option 2: Using ROW_NUMBER()
SELECT Name, Salary
FROM (
    SELECT Name, Salary,
           ROW_NUMBER() OVER (ORDER BY Salary DESC) AS rn
    FROM Employees
) AS temp
WHERE rn = 2;

-- 4. Second Lowest Salary
SELECT MIN(Salary) AS SecondLowestSalary
FROM Employees
WHERE Salary > (SELECT MIN(Salary) FROM Employees);

-- 5. Top 3 Highest Salaries
SELECT DISTINCT Salary
FROM Employees
ORDER BY Salary DESC
LIMIT 3;

-- 6. Top 3 Lowest Salaries
SELECT DISTINCT Salary
FROM Employees
ORDER BY Salary ASC
LIMIT 3;

-- 7. Employees with Highest Salary
SELECT *
FROM Employees
WHERE Salary = (SELECT MAX(Salary) FROM Employees);

-- 8. Employees with Lowest Salary
SELECT *
FROM Employees
WHERE Salary = (SELECT MIN(Salary) FROM Employees);

-- 9. Employees with Salary Above Average
SELECT *
FROM Employees
WHERE Salary > (SELECT AVG(Salary) FROM Employees);

-- 10. Employees with Salary Below Average
SELECT *
FROM Employees
WHERE Salary < (SELECT AVG(Salary) FROM Employees);

---

# SQL Date Functions & Queries – Interview Revision Notes
**Current date reference:** February 16, 2026

## 🟦 Date & Time – Most Asked Patterns (One Table Example)

-- Step 1: Create a sample table (Employees) with dates
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    join_date DATE,
    birth_date DATE,
    last_login DATETIME
);

**Assumed Table:** `employees` (already exists with below sample data)

**Sample Data (for understanding – imagine it's in your DB):**

| emp_id | name   | join_date  | birth_date | last_login          |
|--------|--------|------------|------------|---------------------|
| 101    | Ali    | 2024-05-10 | 1995-03-22 | 2026-02-15 09:30:00 |
| 102    | Rahul  | 2025-01-05 | 1998-11-15 | 2026-02-14 14:45:00 |
| 103    | Sneha  | 2025-02-01 | 2000-07-08 | 2026-02-16 10:15:00 |
| 104    | Priya  | 2024-12-20 | 1992-04-30 | 2026-02-10 18:20:00 |

### Core Date Functions Quick Reference

| Purpose                        | MySQL Syntax                              | Output Example (on 2026-02-16)     |
|--------------------------------|-------------------------------------------|-------------------------------------|
| Today’s date                   | `CURDATE()`                               | 2026-02-16                          |
| Current date + time            | `NOW()`                                   | 2026-02-16 14:30:00                 |
| Extract date only              | `DATE(NOW())`                             | 2026-02-16                          |
| Days between two dates         | `DATEDIFF('2026-02-20', '2026-02-10')`    | 10                                  |
| Add days/months                | `DATE_ADD(NOW(), INTERVAL 7 DAY)`         | 2026-02-23                          |
| Subtract days                  | `DATE_SUB(CURDATE(), INTERVAL 30 DAY)`    | 2026-01-17                          |
| Format date                    | `DATE_FORMAT(join_date, '%d %b %Y')`      | 10 May 2024                         |

### 10 Most Asked Date Queries (Ready to Copy-Paste)

```sql
-- 1. Employees who joined BETWEEN two specific dates (inclusive)
SELECT name, join_date
FROM employees
WHERE join_date BETWEEN '2025-01-01' AND '2025-02-28'
ORDER BY join_date;
-- Output:
-- Rahul → 2025-01-05
-- Sneha → 2025-02-01

-- 2. Last 7 days login activity (including today)
SELECT name, last_login
FROM employees
WHERE last_login >= DATE_SUB(CURDATE(), INTERVAL 7 DAY)
ORDER BY last_login DESC;
-- Output (on 2026-02-16):
-- Sneha → 2026-02-16 10:15:00
-- Ali   → 2026-02-15 09:30:00
-- Rahul → 2026-02-14 14:45:00

-- 3. Employees who joined in the last 30 days
SELECT name, join_date
FROM employees
WHERE join_date >= DATE_SUB(CURDATE(), INTERVAL 30 DAY);

-- 4. Calculate age in years (as of today)
SELECT 
    name,
    FLOOR(DATEDIFF(CURDATE(), birth_date) / 365.25) AS age_years
FROM employees;
-- Approximate output (2026-02-16):
-- Priya → 33
-- Ali   → 30
-- Rahul → 27
-- Sneha → 25

-- 5. Employees born in the current month (February)
SELECT name, birth_date
FROM employees
WHERE MONTH(birth_date) = MONTH(CURDATE());

-- 6. Show date after adding/subtracting intervals
SELECT 
    name,
    join_date,
    DATE_ADD(join_date, INTERVAL 90 DAY)  AS after_3_months,
    DATE_SUB(CURDATE(), INTERVAL 1 YEAR) AS one_year_ago
FROM employees;
-- Example (Ali):
-- join_date: 2024-05-10 → after_3_months: 2024-08-08
-- one_year_ago: 2025-02-16

-- 7. Tenure in days (days since joining)
SELECT 
    name,
    join_date,
    DATEDIFF(CURDATE(), join_date) AS days_employed
FROM employees
ORDER BY days_employed DESC;
-- Example output (2026-02-16):
-- Priya → ~423 days
-- Rahul → ~407 days
-- Ali   → ~282 days
-- Sneha → ~15 days

-- 8. This month's joiners
SELECT name, join_date
FROM employees
WHERE MONTH(join_date) = MONTH(CURDATE())
  AND YEAR(join_date) = YEAR(CURDATE());

-- 9. Nicely formatted dates
SELECT 
    name,
    DATE_FORMAT(join_date, '%d %b %Y')          AS formatted_join,
    DATE_FORMAT(last_login, '%d-%m-%Y %H:%i')   AS login_time
FROM employees;
-- Example:
-- Ali   → 10 May 2024    | 15-02-2026 09:30
-- Rahul → 05 Jan 2025    | 14-02-2026 14:45

-- 10. Employees who joined more than 1 year ago
SELECT name, join_date
FROM employees
WHERE join_date < DATE_SUB(CURDATE(), INTERVAL 1 YEAR);
-- Output:
-- Ali   → 2024-05-10
-- Priya → 2024-12-20
