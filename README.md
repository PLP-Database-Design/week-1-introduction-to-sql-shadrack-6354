# SQL Assignment Week 1


## *What You'll Need*
- A computer with internet access.
- A code editor (e.g., Visual Studio Code).
- MySQL Workbench or another SQL database environment.

---



## *Submission Instructions*
1. Answer every question below and put your responses in a file named `answers.md`
2. Push your completed `answers.md` file to your GitHub repository.
3. Submit the GitHub link for review.

---

## **Assignment Questions**

1. State and Explain the components of a DBMS(Database Management System)
2.  Database Management System (DBMS) is a software system designed to manage, store, and organize data in databases, and provide a way for users and applications to interact with the data in a structured way. The DBMS facilitates data access, data integrity, security, and backup while ensuring that data is stored efficiently. Below are the key components of a DBMS:

1. Database Engine
Definition: The database engine is the core component of the DBMS. It is responsible for managing the storage, retrieval, and manipulation of data within the database.
Explanation: The engine handles all the low-level operations like reading from and writing to the disk. It controls data processing, ensuring that data can be stored and retrieved efficiently and that operations like querying, updating, and deleting are performed without errors.
Examples: MySQL's storage engine, PostgreSQL's engine, Oracle's DB engine.
2. Database Schema
Definition: The database schema defines the structure of the database, including how data is organized and the relationships between different data entities (tables, views, indexes, etc.).
Explanation: The schema is a blueprint or architecture of the database. It defines how data is categorized, what types of data are allowed, and how different entities are related (e.g., tables, columns, and foreign keys). This ensures consistency and integrity of the data stored in the DBMS.
Examples: Table definitions (columns, data types), relationships (one-to-many, many-to-many).
3. Query Processor
Definition: The query processor is responsible for interpreting and executing SQL (Structured Query Language) queries issued by users or applications.
Explanation: It translates high-level user requests (SQL queries) into low-level operations that the DBMS can execute. This includes parsing the query, optimizing it for performance, and then executing it against the stored data. It can include operations like filtering, sorting, joining, and grouping data.
Examples: SQL query execution engine, query optimization.
4. Data Dictionary
Definition: The data dictionary (also known as the system catalog) is a repository of metadata — data about the database itself, including information about tables, columns, data types, indexes, and relationships.
Explanation: The data dictionary stores information on the database structure, constraints, and access rights. It serves as a reference for the DBMS to understand the database schema and how to interact with the data. It helps maintain the integrity and consistency of the database by ensuring that any operations conform to the schema.
Examples: Information about tables, columns, views, and constraints.
5. Transaction Management
Definition: Transaction management ensures that database operations are executed in a way that guarantees consistency and integrity of the data, even in the event of system failures.
Explanation: A transaction is a sequence of operations that must be executed as a single unit. Transaction management ensures that either all the operations in a transaction are completed (commit), or none are (rollback) if there is an error. It adheres to the ACID properties (Atomicity, Consistency, Isolation, Durability) to maintain data integrity.
Examples: Commit, rollback, transaction logs.

3. What is a relational database? Give 4 examples.
4. A relational database stores data in tables with rows and columns, and supports relationships between tables using keys.
Examples of relational databases include MySQL, PostgreSQL, Microsoft SQL Server, and Oracle Database. These systems are widely used for applications that require structured data storage, consistency, and complex querying.




5. State and Explain three classifications of SQL?
6. 1. Data Definition Language (DDL)
Purpose: DDL is used to define, modify, or remove database structures such as tables, indexes, and schemas.
Explanation: DDL commands define the structure of a database by creating, altering, or deleting tables, views, and other objects. These commands do not manipulate the data itself but control the structure and schema of the database.
Key DDL Commands:

CREATE: Used to create database objects like tables, views, indexes, and schemas.
Example: CREATE TABLE employees (id INT, name VARCHAR(100));
ALTER: Used to modify an existing database object, such as adding a column to a table.
Example: ALTER TABLE employees ADD email VARCHAR(100);
DROP: Used to delete an existing database object.
Example: DROP TABLE employees;
TRUNCATE: Used to remove all rows from a table without affecting the table structure.
Example: TRUNCATE TABLE employees;
2. Data Manipulation Language (DML)
Purpose: DML is used to manipulate the data within the database. It allows users to retrieve, insert, update, and delete data in the database tables.
Explanation: DML commands interact with the actual data stored in the tables. These commands allow users to perform CRUD (Create, Read, Update, Delete) operations on the data.
Key DML Commands:

SELECT: Used to query and retrieve data from one or more tables.
Example: SELECT * FROM employees WHERE id = 1;
INSERT: Used to add new rows of data into a table.
Example: INSERT INTO employees (id, name, email) VALUES (1, 'John Doe', 'john@example.com');
UPDATE: Used to modify existing data in a table.
Example: UPDATE employees SET email = 'john.doe@example.com' WHERE id = 1;
DELETE: Used to remove data from a table.
Example: DELETE FROM employees WHERE id = 1;
3. Data Control Language (DCL)
Purpose: DCL is used to control access to data in the database by defining user permissions and rights.
Explanation: DCL commands are concerned with granting or revoking privileges to users, enabling access control to the database. These commands allow administrators to grant or restrict access to the database's data and objects.
Key DCL Commands:

GRANT: Used to give specific privileges (such as SELECT, INSERT, UPDATE) to a user or role.
Example: GRANT SELECT, INSERT ON employees TO user1;
REVOKE: Used to remove previously granted privileges from a user or role.
Example: REVOKE SELECT ON employees FROM user1;

7. What is the difference between a Primary Key and a Foreign Key?
8. Primary Key: A field or combination of fields that uniquely identifies each record in a table. It cannot contain NULL values and ensures that data is uniquely identifiable.
Foreign Key: A field or combination of fields that establishes a link between two tables by referencing the primary key of another table. It can contain NULL values and helps maintain referential integrity across related tables.

9. What is an Entity-Relationship Diagram?
10. An Entity-Relationship Diagram (ERD) is a visual representation of the entities within a system and the relationships between them. It is used in database design to model and structure data in a way that reflects the real-world entities and how they interact with one another. ERDs are widely used in database design and systems analysis to help developers and stakeholders understand the data requirements and relationships of a system before implementation.



11. What are the advantages of relational databases?
12. . Data Integrity
Consistency and Accuracy: Relational databases enforce data integrity through constraints like primary keys, foreign keys, and unique keys, which ensure that the data is consistent and accurate. This helps prevent errors, such as duplicate entries or invalid data.
Referential Integrity: Foreign keys maintain relationships between tables, ensuring that data in one table corresponds correctly to data in related tables. For example, an order in an Orders table must refer to a valid Customer in the Customers table.
2. Flexibility in Data Queries
Powerful Query Language (SQL): Relational databases use SQL (Structured Query Language) for querying, which provides a powerful, flexible, and standardized way to interact with the data. SQL allows users to perform complex queries, such as filtering, sorting, joining tables, aggregating data, and more.
Complex Relationships: SQL queries can handle complex relationships between tables, allowing users to retrieve data across multiple tables through JOINs (e.g., INNER JOIN, LEFT JOIN, etc.).
3. Data Redundancy Reduction
Normalization: Relational databases are designed to reduce data redundancy (duplicate data) through a process called normalization, where data is split across multiple related tables, and relationships are established between them. This minimizes the chances of storing the same data in multiple places, saving storage space and reducing the risk of inconsistencies.
For example, instead of storing customer information with each order, customer details can be stored in a separate Customers table and referenced via a foreign key in the Orders table.
4. Scalability
Horizontal and Vertical Scaling: While traditional relational databases are often associated with vertical scaling (adding more resources to a single server), modern relational database systems can also scale horizontally, supporting large volumes of data and users. Many relational databases offer clustering and partitioning options to distribute data across multiple servers.
Efficient Indexing: Relational databases support indexing, which helps speed up queries, particularly on large datasets. Indexes allow the database to quickly locate rows without scanning the entire table.
5. Security and Access Control
Granular Security Controls: Relational databases support strong security features, including user authentication, role-based access control, and permission management. You can grant or revoke specific permissions for different users or user roles (e.g., read-only access, data modification permissions).
Data Encryption: Many relational database systems provide options for encrypting data at rest (stored data) and in transit (data being transferred between the database and users), enhancing security.

13. State four types of data type used to store data in tables?
14. These data types—integer, character/string, date/time, and floating-point/decimal—are commonly used in relational databases to represent different kinds of data efficiently. The choice of data type is important for ensuring data integrity, optimizing performance, and ensuring that the data is stored in the correct format.
   
15. What is the purpose of a database management system (DBMS)?
16. The primary purpose of a DBMS is to provide a structured, efficient, secure, and reliable environment for managing data. It abstracts the complexities of data storage and retrieval, ensuring that data is organized, accessible, and protected from issues like redundancy, inconsistency, and unauthorized access. By supporting functions like data integrity, security, backup/recovery, and query optimization, DBMS systems are integral to the development and maintenance of modern applications and enterprise systems. 

*How to edit a [markdownfile](https://www.markdownguide.org/basic-syntax/#headings)*

###  NOTE: You should not fork the repository
