# Relational Model Constraints — Advanced Topic

## 1. Introduction

**Relational Model Constraints** are rules or restrictions that data must follow in a relational database.

Constraints help implement business rules and maintain **data integrity**, ensuring that data remains valid and meaningful.

The six constraints covered in this lesson are:

1. Entity Integrity Constraint
2. Referential Integrity Constraint
3. Semantic Integrity Constraint
4. Domain Constraint
5. Null Constraint
6. Check Constraint

## 2. Entity Integrity Constraint

The **Entity Integrity Constraint** ensures that every row in a relation can be uniquely identified using a primary key.

### Key Points

- A primary key uniquely identifies each row (tuple).
- Primary key values cannot be duplicated.
- A primary key cannot contain `NULL` values.
- Indexes are used to implement the uniqueness constraint, as explained in the lesson.

### Example

Consider an `Author` table:

| Author_ID (PK) | Author_Name | City |
|---|---|---|
| A1 | Raoul Chong | Toronto |
| A2 | Amit Kumar | Delhi |
| A3 | Priya Sharma | Mumbai |

Here, `Author_ID` is the primary key.

If two authors have a `NULL` value instead of their IDs, it becomes impossible to distinguish them reliably using that key.

Therefore, primary key attributes cannot accept `NULL` values.

**Remember:** Primary key = Unique identification + No `NULL` values.

## 3. Referential Integrity Constraint

The **Referential Integrity Constraint** defines relationships between tables and ensures that those relationships remain valid.

It uses primary keys and foreign keys to maintain data validity.

### Example

**Author Table**

| Author_ID (PK) | Author_Name |
|---|---|
| A1 | Raoul Chong |
| A2 | Amit Kumar |

**Book Table**

| Book_ID (PK) | Book_Title | Author_ID (FK) |
|---|---|---|
| B1 | SQL Basics | A1 |
| B2 | Database Design | A2 |

In this example:
- `Author_ID` is the primary key in `Author`.
- `Author_ID` is a foreign key in `Book`.
- The foreign key connects a book record to an author record.

Referential integrity helps prevent invalid references to records that do not exist in the referenced table.

## 4. Semantic Integrity Constraint

The **Semantic Integrity Constraint** concerns the correctness and meaning of data.

Data should represent meaningful and correct information.

### Example

Suppose the `Author` table contains a `City` attribute.

| Author_ID | Author_Name | City |
|---|---|---|
| A1 | Raoul Chong | Toronto |
| A2 | Amit Kumar | Delhi |
| A3 | Priya Sharma | Garbage |

The value `Garbage` does not represent a meaningful city in this example.

Semantic integrity concerns whether the stored information is meaningful and correct.

**Remember:** Semantic integrity = Correct meaning of data.

## 5. Domain Constraint

A **Domain Constraint** specifies the permissible values for an attribute.

It defines what type or range of values an attribute is allowed to contain.

### Example: Country Attribute

Suppose the `Country` attribute must contain a two-letter country code.

| Author_ID | Country |
|---|---|
| A1 | CA |
| A2 | IN |
| A3 | 34 |

Here:
- `CA` represents Canada.
- `IN` represents India.
- `34` is invalid under the specified two-letter code rule.

The domain constraint restricts the attribute to permitted values.

**Remember:** Domain constraint = Allowed values for an attribute.

## 6. Null Constraint

The **Null Constraint** specifies that an attribute cannot contain `NULL` values.

A `NULL` value generally indicates missing, unknown, or unavailable information.

### Example

Suppose every author must have a first name and last name.

| Author_ID | First_Name | Last_Name |
|---|---|---|
| A1 | Raoul | Chong |
| A2 | Amit | Kumar |
| A3 | NULL | Sharma |

In this example, the third author's first name is `NULL`, which violates the rule that first and last names must be provided.

A null constraint can be implemented in SQL using `NOT NULL`.

```sql
CREATE TABLE Author (
    Author_ID CHAR(2) PRIMARY KEY,
    First_Name VARCHAR(50) NOT NULL,
    Last_Name VARCHAR(50) NOT NULL
);
```

**Remember:** Null constraint = Attribute must not contain `NULL`.

## 7. Check Constraint

The **Check Constraint** limits the values accepted by an attribute using a specified condition.

It helps enforce domain integrity by rejecting values that do not satisfy the condition.

### Example: Book Publication Year

Suppose a `Book` table contains a `Year` attribute representing the year a book was published.

The publication year should not be greater than the current year.

A check constraint can enforce this rule.

```sql
CREATE TABLE Book (
    Book_ID INT PRIMARY KEY,
    Title VARCHAR(100),
    Year INT CHECK (Year <= 2010)
);
```

In this example, the year cannot exceed 2010. This illustrates the lesson's example, which assumes the current year is 2010.

For a modern database, the rule would need to be updated or implemented using an appropriate current-year condition.

**Remember:** Check constraint = A condition that values must satisfy.

## 8. Comparison of the Six Constraints

| Constraint | Purpose | Example |
|---|---|---|
| Entity Integrity | Uniquely identifies each row and prevents `NULL` primary keys. | `Author_ID` is a primary key. |
| Referential Integrity | Maintains valid relationships between tables. | `Book.Author_ID` references `Author.Author_ID`. |
| Semantic Integrity | Ensures that data has correct and meaningful content. | A city value should represent a valid city. |
| Domain Constraint | Restricts values to an allowed domain. | Country must use a two-letter code. |
| Null Constraint | Prevents `NULL` values in specified attributes. | First name must be provided. |
| Check Constraint | Requires values to satisfy a condition. | Publication year must not exceed a specified year. |

## 9. Quick Revision Questions

**Q1. What is a database constraint?**

A rule or restriction that data must follow in a database.

**Q2. How many constraints are covered in this lesson?**

Six.

**Q3. Which constraint prevents primary key attributes from containing `NULL` values?**

Entity Integrity Constraint.

**Q4. Which constraint maintains valid relationships between tables?**

Referential Integrity Constraint.

**Q5. Which constraint focuses on the correctness and meaning of data?**

Semantic Integrity Constraint.

**Q6. Which constraint specifies permissible values for an attribute?**

Domain Constraint.

**Q7. Which constraint prevents specified attributes from containing `NULL` values?**

Null Constraint.

**Q8. Which constraint enforces a condition on accepted values?**

Check Constraint.

**Q9. What is the difference between Entity Integrity and Null Constraint?**

Entity Integrity requires primary key attributes to be unique and non-`NULL`. A Null Constraint can prevent `NULL` values in other specified attributes as well.

**Q10. What is the difference between Domain and Check Constraints?**

A domain constraint defines permissible attribute values. A check constraint enforces a condition that values must satisfy. They can overlap in practice.

## 10. Summary

The six relational model constraints help maintain data integrity:

- **Entity Integrity:** Primary keys must uniquely identify rows and cannot be `NULL`.
- **Referential Integrity:** Relationships between tables must remain valid.
- **Semantic Integrity:** Data should be meaningful and correct.
- **Domain Constraint:** Values must belong to the permitted domain.
- **Null Constraint:** Specified attributes cannot contain `NULL`.
- **Check Constraint:** Values must satisfy a defined condition.

Understanding these constraints is essential for designing reliable relational databases and writing correct SQL statements.
