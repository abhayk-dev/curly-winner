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
