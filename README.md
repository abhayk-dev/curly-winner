# 🗄️ IBM SkillsBuild: SQL & Relational Databases

This directory contains my study notes, foundational database concepts, and query scripts compiled during the IBM Relational Database curriculum.

---

## 🧠 Core Relational Database Concepts

### 1. The Relational Model
* **RDBMS:** Relational Database Management Systems store data in structured tables consisting of rows (tuples) and columns (attributes).
* **Primary Key (PK):** A unique identifier for each record in a table. It cannot contain `NULL` values.
* **Foreign Key (FK):** A field in one table that links to the Primary Key of another table, establishing a relationship between them.

### 2. Database Design & Normalization
* **ER Diagrams (ERD):** Entity-Relationship Diagrams visually map out how database tables connect via one-to-one, one-to-many, or many-to-many relationships.
* **Normalization:** The process of organizing data to reduce redundancy and improve data integrity (1NF, 2NF, 3NF).

### 3. ACID Properties
To ensure reliable transaction processing, relational databases adhere to:
* **Atomicity:** All parts of a transaction succeed, or the entire transaction fails (All-or-Nothing).
* **Consistency:** Data must meet all validation rules and constraints before and after a transaction.
* **Isolation:** Multiple transactions can execute concurrently without interfering with each other.
* **Durability:** Once a transaction is committed, it remains saved even in the event of a system crash.

---

## 🛠️ SQL Syntax Reference Cheat Sheet

### Data Definition Language (DDL)
Used to define or modify the database structure.
```sql
-- Creating a table with constraints
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    hire_date DATE,
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES departments(department_id)
);
```

### Data Manipulation Language (DML)
Used to manage data within the objects.
```sql
-- Inserting a new record
INSERT INTO employees (employee_id, first_name, last_name, hire_date, department_id)
VALUES (101, 'Jane', 'Doe', '2026-03-15', 4);
```

### Data Query Language (DQL) - Joins & Aggregations
Used to retrieve specific data from the database.
```sql
-- Fetching data across tables using an INNER JOIN
SELECT e.first_name, e.last_name, d.department_name
FROM employees e
INNER JOIN departments d 
ON e.department_id = d.department_id
WHERE e.hire_date > '2025-01-01';
```

---

## 📂 Practice Scripts Index
* `[01_ddl_commands.sql](./practice_queries/01_ddl_commands.sql)` - Table creation, altering schemas, and drops.
* `[02_basic_queries.sql](./practice_queries/02_basic_queries.sql)` - `SELECT`, `WHERE`, `ORDER BY`, and arithmetic operations.
* `[03_joins_aggregations.sql](./practice_queries/03_joins_aggregations.sql)` - Multi-table operations, `GROUP BY`, and `HAVING` clauses.
