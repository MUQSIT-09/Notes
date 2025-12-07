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

**Example Image:**  
![DBMS Overview](https://www.istockphoto.com/photo/question-mark-database-3d-icon-gm1479478181-507449841?utm_source=pixabay&utm_medium=affiliate&utm_campaign=sponsored_image&utm_content=srp_topbanner_media&utm_term=what+is+dbms)

---

## 🟦 2. Data Models in DBMS
Data models define how data is logically structured.

- **Hierarchical Model:** Data organized in a tree-like structure.  
- **Network Model:** Multiple parent-child relationships (graph-based).  
- **Relational Model:** Data stored in tables (relations).  
- **Object-Oriented Model:** Data represented as objects.

**Example Image:**  
![Data Models](https://usemynotes.com/data-model-in-dbms-database-management-system/)

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

| DBMS | RDBMS |
|------|--------|
| No relations between data | Tables have relationships |
| No constraints | Supports primary/foreign keys |
| Unstructured data | Structured schema |
| Examples: XML DB, File System | MySQL, SQL Server, Oracle |

**Diagram:**  
![DBMS vs RDBMS](https://medium.com/@manojlasantha306/dbms-vs-rdbms-the-differences-explained-c65b91baa7f1)

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

|                Students               |          |         Departments       |
|---------------------------------------|          |---------------------------|
| **StudentID** | **Name** | **DeptID** | **→→→**  | **DeptID** | **DeptName** |
| 101           | Alice    |    D01     |          |     D01    |     CS       |
| 102           | Bob      |    D02     |          |     D02    |     EE       |

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

**Diagram:**  
![Normalization](data:image/jpeg;base64,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)

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
![ER Diagram](https://tutorialwing.com/er-diagram-in-dbms-components-symbol-and-notations/)

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

**Visual:**  
![Indexes](https://cdn1.byjus.com/wp-content/uploads/2022/05/word-image195.png)
     
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


