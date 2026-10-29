# Introduction to Relational Model Constraints

## 1. Introduction

**Relational Model Constraints** are rules or restrictions that data must follow in a relational database.

These rules help maintain data integrity and establish relationships between tables.

In this lesson, we learn about:
- Referencing
- Primary keys
- Foreign keys
- Parent tables
- Dependent (child) tables

## 2. Referencing

**Referencing** is the process in which one entity or table refers to another entity or table to access related information.

### Example: Book and Author

Consider a simplified library database containing two entities:

- `Book`
- `Author`

The `Book` entity refers to the `Author` entity to look up author information.

Similarly, the `Author` entity may refer to the `Book` entity to look up book information.

In a relational data model, this is called **referencing**.

Referencing helps establish data integrity between two relations.

## 3. Primary Key (PK)

A **Primary Key** is an attribute or set of attributes that uniquely identifies each row in a table.

### Key Points
- Every row must be uniquely identifiable.
- A primary key cannot contain duplicate values.
- A primary key is used to identify individual records.

### Example

| Author_ID (PK) | Author_Name |
|---|---|
| A01 | Rahul |
| A02 | Amit |
| A03 | Priya |

Here, `Author_ID` is the primary key because it uniquely identifies each author record.

Other examples of primary key attributes include:
- `Book_ID`
- `Borrower_ID`

## 4. Foreign Key (FK)

A **Foreign Key** is an attribute or set of columns that refers to the primary key of another table.

Foreign keys help establish relationships between tables.

### Example

**Author Table**

| Author_ID (PK) | Author_Name |
|---|---|
| A01 | Rahul |
| A02 | Amit |

**Book Table**

| Book_ID (PK) | Book_Title | Author_ID (FK) |
|---|---|---|
| B01 | SQL Basics | A01 |
| B02 | Database Design | A02 |

In this example:
- `Author_ID` is the primary key in the `Author` table.
- `Book_ID` is the primary key in the `Book` table.
- `Author_ID` in the `Book` table is a foreign key referencing the `Author` table.

This allows a book record to be associated with an author record.

## 5. Primary Key vs. Foreign Key

| Primary Key (PK) | Foreign Key (FK) |
|---|---|
| Uniquely identifies each row in its table. | Refers to a primary key in another table. |
| Identifies records. | Establishes relationships between tables. |
| Example: `Author_ID` in Author. | Example: `Author_ID` in Book. |

## 6. Parent Table

A **Parent Table** is a table containing a primary key that is referenced by at least one foreign key in another table.

### Example

The `Author` table can be a parent table when another table references its primary key.

Similarly, the `Book` table can also be a parent table when another table references its primary key.

### Example Structure

- `Author` → Parent table
- `Book` → Parent table

A table's role as a parent depends on its relationship with other tables.

## 7. Dependent Table (Child Table)

A **Dependent Table**, also called a **Child Table**, is a table containing one or more foreign keys.

These foreign keys refer to parent tables.

### Example: Author_List

Suppose the `Author_List` table contains:
- `Author_ID` (FK)
- `Book_ID` (FK)

The `Author_List` table references both:
- `Author`
- `Book`

Therefore, `Author_List` is a dependent (child) table.

## 8. One-to-Many Relationship

A **one-to-many relationship** means that one record in a parent table can be associated with multiple records in a related table.

For example, in a library database, one author may be associated with multiple book records.

A foreign key is commonly used on the many side of this relationship to reference the parent table.

**Example:**

One `Author` → Multiple `Book` records

The lesson also identifies one-to-many relationships among the related entities in its library database model.

## 9. Example: Library Database Structure

A simplified library database may contain the following entities:

- `Author`
- `Book`
- `Borrower`
- `Loan`
- `Copy`
- `Author_List`

The primary key attributes identify records, while foreign keys connect related tables.

For example:
- `Author_ID` identifies an author.
- `Book_ID` identifies a book.
- `Borrower_ID` identifies a borrower.
- `Copy` may contain `Book_ID` as a foreign key.
- `Author_List` may contain foreign keys referring to `Author` and `Book`.

## 10. Quick Revision

**Q1. What is referencing?**

Referencing is when one entity or table refers to another to access related information.

**Q2. What is a primary key?**

A primary key uniquely identifies each row in a table.

**Q3. What is a foreign key?**

A foreign key is a column or set of columns that refers to a primary key in another table.

**Q4. What is a parent table?**

A table whose primary key is referenced by at least one foreign key in another table.

**Q5. What is a dependent table?**

A table containing one or more foreign keys that refer to parent tables.

**Q6. What is another name for a dependent table?**

A child table.

**Q7. What is the purpose of referencing?**

It establishes relationships and helps maintain data integrity between relations.

**Q8. Give an example of a dependent table.**

`Author_List`, which contains foreign keys referring to `Author` and `Book`.

## 11. Summary

Remember these important terms:

- **Referencing:** Connecting related entities or tables.
- **Primary Key (PK):** Uniquely identifies a row.
- **Foreign Key (FK):** Refers to a primary key in another table.
- **Parent Table:** A table whose key is referenced by another table.
- **Dependent/Child Table:** A table containing foreign keys.
- **One-to-Many:** One parent record can relate to multiple records in another table.

These concepts are essential for understanding relational database design and maintaining data integrity.
