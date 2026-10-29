# Relational Model Concepts

## 1. Introduction

The **Relational Model** is a database model based on mathematical concepts, especially relations and sets.

- The relational model was first proposed in **1970**.
- It is based on mathematical terms and concepts.
- Its main building blocks are **relations and sets**.
- A relational database is a collection of relations.

## 2. Important Terms

### 2.1 Relation

A **relation** is a mathematical concept based on sets. In relational databases, it is the mathematical term for a table.

A table consists of:
- Rows
- Columns

**Example:**

| Author_ID | First_Name | City |
|---|---|---|
| A01 | Rahul | Delhi |
| A02 | Amit | Mumbai |

In this example, the table represents a relation.

### 2.2 Set

A **set** is an unordered collection of distinct elements of the same type.

Important properties of a set:
- **Unordered:** Elements have no defined order.
- **No duplicates:** Every element is distinct.
- **Same type:** A set contains items of the same type, as described in the lesson.

### 2.3 Relational Database

A **relational database** is a collection of relations (tables).

Each relation stores data in rows and columns.

## 3. Parts of a Relation

A relation consists of two main parts:

1. Relational Schema
2. Relational Instance

## 4. Relational Schema

A **Relational Schema** defines the structure of a relation.

It specifies:
- The name of the relation.
- The names of its attributes (columns).
- The data type of each attribute.

### Example: Author Schema

Consider an `Author` relation with these attributes:

| Attribute | Data Type | Description |
|---|---|---|
| Author_ID | CHAR | Fixed-length character string |
| Last_Name | VARCHAR | Variable-length character string |
| First_Name | VARCHAR | Variable-length character string |
| Email | VARCHAR | Variable-length character string |
| City | VARCHAR | Variable-length character string |
| Country | CHAR | Fixed-length character string |

Here:
- `Author` is the relation name.
- The attributes define the table's columns.
- `CHAR` stores fixed-length character strings.
- `VARCHAR` stores variable-length character strings.

Together, the relation name, attributes, and their data types form the relational schema.

## 5. Relational Instance

A **Relational Instance** is the actual table containing rows and columns at a particular point in time.

- **Columns** represent attributes or fields.
- **Rows** represent tuples.
- The rows contain the actual data values.

### Example: Author Instance

| Author_ID | Last_Name | First_Name | Email | City | Country |
|---|---|---|---|---|---|
| A01 | Sharma | Rahul | rahul@example.com | Delhi | India |
| A02 | Verma | Amit | amit@example.com | Mumbai | India |
| A03 | Singh | Priya | priya@example.com | Jaipur | India |

This table is an illustrative example of a relational instance.

## 6. Relational Schema vs. Relational Instance

| Relational Schema | Relational Instance |
|---|---|
| Defines the structure of a relation. | Represents the actual table data. |
| Specifies the relation name. | Contains the data records. |
| Defines attributes and their data types. | Contains rows and columns. |
| Describes how the table is structured. | Shows the data stored in that structure. |

**Easy way to remember:**

- **Schema = Structure**
- **Instance = Actual data**

## 7. Degree of a Relation

**Degree** refers to the number of attributes (columns) in a relation.

For example, if an `Author` table has six columns, its degree is 6.

\[
\text{Degree} = \text{Number of columns}
\]

## 8. Cardinality of a Relation

**Cardinality** refers to the number of tuples (rows) in a relation.

For example, if an `Author` table contains five data rows, its cardinality is 5.

\[
\text{Cardinality} = \text{Number of rows}
\]

## 9. Example: Degree and Cardinality

Consider the following table:

| Author_ID | Last_Name | First_Name | Email | City | Country |
|---|---|---|---|---|---|
| A01 | Sharma | Rahul | r@example.com | Delhi | India |
| A02 | Verma | Amit | a@example.com | Mumbai | India |
| A03 | Singh | Priya | p@example.com | Jaipur | India |
| A04 | Kumar | Neha | n@example.com | Pune | India |
| A05 | Gupta | Ravi | g@example.com | Lucknow | India |

In this example:

- Number of columns = 6
- Number of data rows = 5
- **Degree = 6**
- **Cardinality = 5**

Note: The header row is not counted as a data tuple.

## 10. Quick Revision

**Q1. When was the relational model first proposed?**

In 1970.

**Q2. What is a relation?**

A mathematical concept based on sets and the mathematical term for a table in a relational database.

**Q3. What is a set?**

An unordered collection of distinct elements.

**Q4. What is a relational schema?**

The structure of a relation, including its name, attributes, and data types.

**Q5. What is a relational instance?**

The table containing actual data in rows and columns.

**Q6. What is a tuple?**

A row in a relation.

**Q7. What is an attribute?**

A column or field in a relation.

**Q8. What is degree?**

The number of attributes or columns in a relation.

**Q9. What is cardinality?**

The number of tuples or rows in a relation.

**Q10. What is the difference between CHAR and VARCHAR?**

- `CHAR`: Fixed-length character string.
- `VARCHAR`: Variable-length character string.

## 11. Summary

The relational model organizes data into relations (tables) using mathematical concepts.

Remember these key definitions:

- **Relation:** Table
- **Set:** Unordered collection of distinct elements
- **Schema:** Table structure
- **Instance:** Actual table data
- **Attribute:** Column
- **Tuple:** Row
- **Degree:** Number of columns
- **Cardinality:** Number of data rows

These concepts form the foundation for understanding relational databases and SQL.
