# Normalization
Normalization in the context of relational database management systems (RDBMS) is a process of organizing data in a database to reduce redundancy and dependency. The goal of normalization is to design a database schema that minimizes data redundancy and ensures data integrity. This is achieved by breaking down large tables into smaller, related tables and defining relationships between them. The process is typically carried out through a series of normal forms.

There are several normal forms (NF) that define the level of normalization, with each successive normal form building on the previous one. The most common normal forms are:

# First Normal Form (1NF):

Eliminate duplicate columns from the same table.

Create a separate table for each set of related data.

Identify a unique column or set of columns (primary key) for each table.

# Second Normal Form (2NF):

Meet the requirements of 1NF.

Remove partial dependencies. 

This means that no column should be dependent on only a portion of a multi-column primary key.

Break the table into smaller tables and establish relationships between them.

# Third Normal Form (3NF):

Meet the requirements of 2NF.
Remove transitive dependencies. This means that no column should be dependent on any other non-key columns.
Further break down tables and establish relationships.
There are higher normal forms beyond 3NF, such as Boyce-Codd Normal Form (BCNF) and Fourth Normal Form (4NF), but they are less commonly used in practice.

# Boyce-Codd Normal Form (BCNF)

BCNF is a stricter form of 3NF that ensures that each determinant in a table is a candidate key. In other words, BCNF ensures that each non-key attribute is dependent only on the candidate key.

The process of normalization helps in achieving the following benefits:

Minimizing data redundancy: Reducing the amount of duplicated data in the database.
Improving data integrity: Ensuring that data is accurate and consistent by avoiding update anomalies.
Simplifying data maintenance: Making it easier to add, delete, or modify data without introducing errors.
It's important to note that while normalization is crucial for maintaining data integrity, there can be cases where denormalization (introducing some level of redundancy) is appropriate for performance optimization. The decision to normalize or denormalize depends on the specific requirements of the application and the trade-offs between data consistency and query performance.

# Fourth Normal Form (4NF)

4NF is a further refinement of BCNF that ensures that a table does not contain any multi-valued dependencies.

# Fifth Normal Form (5NF)

5NF is the highest level of normalization and involves decomposing a table into smaller tables to remove data redundancy and improve data integrity.

Normal forms help to reduce data redundancy, increase data consistency, and improve database performance. However, higher levels of normalization can lead to more complex database designs and queries. It is important to strike a balance between normalization and practicality when designing a database.

# Advantages of Normalization

Normalization helps to minimize data redundancy.

Greater overall database organization.

Data consistency within the database.

Much more flexible database design.

Enforces the concept of relational integrity.

# Disadvantages of Normalization

You cannot start building the database before knowing what the user needs.

The performance degrades when normalizing the relations to higher normal forms, i.e., 4NF, 5NF.

It is very time-consuming and difficult to normalize relations of a higher degree.

Careless decomposition may lead to a bad database design, leading to serious problems.

#  Q-codd Rules for RDBMS

# Rule 0: The Foundation Rule
The DB must be structured in a relational manner so that the system’s relational capabilities can manage the DB.

# Rule 1: The Information Rule
A DB comprises a variety of data, which must be recorded in the form of columns and rows in each and every cell of a table.

# Rule 2: The Guaranteed Access Rule
A relational DB’s primary key value, column name, and table name can be used to conceptually retrieve any single or precise data (the atomic value).

# Rule 3: The Systematic Treatment of Null Values
The treatment of Null values in DB records is defined by this rule. No value in a cell, missing data, unsuitable information, unknown data, the primary key that should not be null, etc., are all examples of null values in DBs.

# Rule 4: The Dynamic/Active Online Catalog on the basis of the Relational Model
A DB dictionary is a logical representation of the whole logical structure of a descriptive DB that needs to be stored online. It grants users access to the DB and uses a query language that is comparable to that of the DB.

# Rule 5: The Comprehensive Data SubLanguage Rule
The relational DB supports a variety of languages, and in order to access the DB, the language has to be linear, explicit, or a well-defined syntax, character strings. It must support the following operations: view definition, integrity constraints, data manipulation, data definition, as well as limit transaction management. It is considered a DB violation if the DB permits access to the data and information without the use of any language.

# Rule 6: The View Updating Rule
A view table can theoretically be updated, and DB systems must update them in practice.

# Rule 7: The Relational Level Operation (or High-Level Insert, Delete, and Update) Rule
In each level or single row, a DB system should adhere to high-level relational operations (for example, update, insert, and delete). The DB system also includes operations like intersection, union, and minus.

# Rule 8: The Physical Data Independence Rule
To access a DB or an application, all stored data must be independent physically. Each piece of data should not be reliant on another piece of data or an application. External applications that access data from the DB will have no effect if data is altered or the physical structure of a given DB is modified.

# Rule 9: The Logical Data Independence Rule
It’s similar to the independence of physical data. It indicates that any modifications made at the logical level (or the table structures) should not have an impact on the user’s experience (application). For example, if a table is split into two separate tables or into two table joins in order to produce a single table, the application at the user view should not be affected.

# Rule 10: The Integrity Independence Rule
When we are using SQL to put data into table cells, a DB must guarantee integrity independence. All the entered values must not be changed, and the integrity of the data should not be reliant on any external component or application. It’s also useful for making each front-end app DB-independent.

# Rule 11: The Distribution Independence Rule
This rule denotes that a DB must function properly even if it’s stored in multiple locations and used by various end-users. Let’s say a person uses an application to access the DB. In such a case, they must not be aware that another user is using the same data, and thus, the data they always obtain is only available on one site. The DB can be accessed by end-users, and each user’s access data must be independent in order for them to run SQL queries.

# Rule 12: The Non-Subversion Rule
RDBMS is defined by this rule as a SQL language for storing and manipulating data in a DB. If a system uses a low-level or different language to access the DB system other than SQL, it should not bypass or subvert data integrity.

Keep learning and stay tuned to get the latest updates on the GATE Exam along with GATE Eligibility Criteria, GATE Syllabus for CSE (Computer Science Engineering), GATE CSE Notes, GATE CSE Question Paper, and more.
