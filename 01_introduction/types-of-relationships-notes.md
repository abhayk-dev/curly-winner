# Types of Relationships — Study Notes

## 1. Learning Objectives

After studying this lesson, you should be able to:
- Describe the building blocks of a relationship.
- Explain the symbols used in a relationship set.
- Distinguish between one-to-one, one-to-many, and many-to-many relationships.

## 2. Building Blocks of Relationships

The lesson identifies these building blocks:
- **Entities / entity sets** — the things being represented, such as `Book` and `Author`.
- **Relationship sets** — describe how entities are associated with one another.
- **Crow’s foot notation** — a notation used to show how many entities can participate in a relationship.

## 3. ER Diagram Symbols

An **Entity-Relationship (ER) diagram** visually represents entities, their attributes, and the relationships between entities.

| Element | Symbol / representation | Meaning |
|---|---|---|
| Entity set | Rectangle | Represents an entity, such as `Book` or `Author` |
| Relationship set | Diamond | Represents a relationship between entities |
| Attribute | Oval | Represents a property of an entity |
| Crow’s foot notation | Symbols such as a less-than-like fork, greater-than-like fork, or vertical line | Indicates relationship cardinality in the notation used by the lesson |

Lines connect related elements in an ER diagram.

## 4. Entities and Attributes

**Attributes** are properties that describe an entity. In the lesson’s examples, attributes are shown as ovals connected to their entity.

### Book entity
Example attributes:
- Title
- Edition
- Year
- Price

### Author entity
Example attributes:
- Last name
- First name
- Email
- City
- Country
- Author ID

The lesson notes that each attribute is connected to exactly one entity. Attributes may be omitted from relationship diagrams when they would make the diagram cluttered.

## 5. Relationship Example: Book and Author

The relationship set used in the example is **`authored-by`**.

The lesson gives these possibilities:
- A book must be written by at least one author.
- A book may be written by two or more authors.
- An author may write one book or multiple books.

The relationship type depends on how many entities can be associated on each side.

## 6. Types of Relationships

### One-to-one (1:1)
- Each entity in the entity set participates in exactly one relationship, as described in the lesson’s example.
- The lesson uses thick lines to indicate participation in at least one and exactly one relationship.

### One-to-many (1:N)
- One entity on one side can be related to multiple entities on the other side.
- In the example, one book can be associated with multiple authors.
- The same relationship can be described from the opposite direction as **many-to-one**: many authors write one book.
- Crow’s foot notation is used to indicate the “many” side.

### Many-to-many (M:N)
- Multiple entities on either side can participate in multiple relationships.
- In the example, many authors can write many books.
- The lesson shows this by placing the “many” symbols on both sides of the relationship set.

## 7. Quick Comparison

| Relationship type | Meaning in the lesson’s example |
|---|---|
| One-to-one (1:1) | One book is related to one author |
| One-to-many (1:N) | One book can be related to multiple authors |
| Many-to-one (N:1) | Multiple authors can be related to one book |
| Many-to-many (M:N) | Multiple books can be related to multiple authors |

## 8. Key Takeaways

- Entities, relationship sets, and crow’s foot notation are the lesson’s stated building blocks of relationships.
- Rectangles represent entities, diamonds represent relationship sets, and ovals represent attributes.
- Attributes describe entities; examples include a book’s title and an author’s email.
- The `authored-by` relationship connects `Book` and `Author`.
- One-to-one, one-to-many, and many-to-many relationships differ by how many entities can be associated on each side.

## 9. Revision Questions

1. What are the three building blocks of a relationship mentioned in the lesson?
2. Which shape represents an entity set in an ER diagram?
3. Which shape represents a relationship set?
4. What is an attribute? Give two examples from the `Book` entity.
5. What is the relationship set used to connect `Book` and `Author`?
6. How does a one-to-many relationship differ from a many-to-many relationship?
7. What does the lesson use thick lines to indicate?
8. Why might attributes be omitted from a relationship diagram?

---

*Source: Notes prepared from the provided video transcript, “Types of Relationships.”*
