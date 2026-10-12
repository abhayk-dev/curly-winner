# SQL and Relational Database 101: Study Notes

### 1. Key Definitions
* **SQL (Structured Query Language):** A computer language used to query and manage data in relational databases (often pronounced "sequel").
* **Data:** A collection of raw facts, numbers, words, or pictures (e.g., names, phone numbers, account balances).
* **Database:** An organized digital program or repository that stores data so it can be kept secure and accessed quickly.
* **Relational Database:** A database that stores data in tabular form—using rows and columns, similar to a spreadsheet—and allows connections between different tables.

### 2. Database Management Systems
* **DBMS (Database Management System):** A set of software tools used to store, organize, and access data in a database.
* **RDBMS (Relational Database Management System):** A DBMS specifically designed for relational databases (using tables and relationships).
* **Examples of RDBMS:**
  * **MySQL**
  * **Oracle Database** 
  * **DB2 Express-C**

### 3. Five Basic SQL Commands
For most database users, these five core commands handle basic operations:
1. **Create a table:** Build a new table structure.
2. **Insert data:** Add new records or rows into the table.
3. **Select data:** Query and retrieve data from the table.
4. **Update data:** Modify existing records in the table.
5. **Delete data:** Remove records or rows from the table.

# Information Models and Data Models: Study Notes

### 1. Information Model vs. Data Model
* **Information Model:** A high-level, conceptual blueprint that defines objects, their properties, and relationships at an abstract level (e.g., how real-world items connect).
* **Data Model:** A concrete, detailed blueprint used to design and build an actual database system.

### 2. Types of Models
* **Hierarchical Model:** Organizes data in a tree structure with a single parent node branching into multiple child nodes. A child node can only have one parent (e.g., an organization chart). 
  * *History:* IBM's Information Management System (1968) was the first hierarchical system, built for the Apollo space program.
* **Relational Model:** The most widely used model today. It stores data in simple table structures.
  * *Core Advantage:* Provides **data independence** (logical data independence, physical data independence, and physical storage independence).
* **Entity-Relationship (ER) Model:** A tool used to design relational databases by mapping out collections of objects and how they interact. 

### 3. Building Blocks of ER Diagrams
The ER Model uses specific visual elements that translate directly into database structures:
* **Entities:** Core objects (people, places, or things) that exist independently. 
  * *Visual:* Represented as **rectangles**.
  * *Database translation:* Becomes a **Table**.
  * *Example:* "Book" or "Author".
* **Attributes:** Properties or data elements that describe the characteristics of an entity.
  * *Visual:* Represented as **ovals** connected to their specific entity.
  * *Database translation:* Becomes the **Columns** inside a table.
  * *Example:* "Book Title" for a Book, or "Email Address" for an Author.
