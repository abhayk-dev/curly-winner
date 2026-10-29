# Mapping Entities to Tables

## 1. Introduction

**Mapping Entities to Tables** is the process of converting an Entity-Relationship Diagram (ERD) into tables in a relational database.

- An **ER Diagram (ERD)** is a basic foundation for designing a database.
- It represents entities and their attributes.
- During database design, we first create an ERD and then map it to database tables.

## 2. Important Terms

### Entity
An entity is an object or concept about which we want to store information.

**Examples:**
- Book
- Author
- Student
- Employee

### Attribute
An attribute is a property or characteristic of an entity.

For example, a `Book` entity may have these attributes:
- Book_ID
- Title
- Author
- Price

### Table
A table stores data in a relational database. It consists of rows and columns.

- **Rows:** Represent individual records.
- **Columns:** Represent attributes or fields.

## 3. How to Map an Entity to a Table

The basic mapping process follows these steps:

1. Start with an Entity-Relationship Diagram (ERD).
2. Identify the entities in the diagram.
3. Create a table for each entity.
4. Convert the entity's attributes into columns.
5. Add data values to the columns to create records.

### Basic Mapping Rule

| ER Diagram | Relational Database |
|---|---|
| Entity | Table |
| Attribute | Column |
| Data values | Values stored in rows |

## 4. Example: Book Entity

Suppose an ERD contains a `Book` entity with the following attributes:

- Book_ID
- Title
- Author
- Price

### Step 1: Identify the Entity

The entity is `Book`.

### Step 2: Create the Table

The entity becomes a table with the same name: `Book`.

### Step 3: Convert Attributes into Columns

Each attribute becomes a column in the table.

| Book_ID | Title | Author | Price |
|---|---|---|---|
| 101 | Database Basics | Rahul | 299 |
| 102 | SQL Fundamentals | Amit | 399 |

The table now contains columns and data records.

## 5. Example: Author Entity

Suppose an ERD contains an `Author` entity.

Its attributes might include:

- Author_ID
- Author_Name
- Country

The entity becomes an `Author` table, and its attributes become columns.

| Author_ID | Author_Name | Country |
|---|---|---|
| 1 | Rahul | India |
| 2 | Amit | India |

Adding data values completes the table's practical representation.

*Note: The Book and Author attributes and sample records above are illustrative examples to help explain the mapping process.*

## 6. Key Points to Remember

- An ERD is used as the starting point for relational database design.
- An entity is mapped to a table.
- The attributes of an entity become the columns of that table.
- Data values are stored in the table's rows.
- A relational database table consists of rows and columns.
- The entity and its table generally have the same name in the examples covered in this lesson.

## 7. Quick Revision

**Q1. What is an ERD?**

An Entity-Relationship Diagram is a diagram used as a foundation for database design.

**Q2. What does an entity become when mapped to a relational database?**

An entity becomes a table.

**Q3. What do attributes become?**

Attributes become columns in the table.

**Q4. What does a table consist of?**

A table consists of rows and columns.

**Q5. What completes the practical table representation?**

Adding data values to the columns creates records in the table.

## 8. Summary

The process of mapping entities to tables converts an ERD into a relational database structure:

**Entity → Table**

**Attribute → Column**

**Data values → Records stored in rows**

This mapping process is an important step in relational database design.
