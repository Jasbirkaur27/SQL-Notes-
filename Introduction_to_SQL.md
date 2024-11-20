### What is SQL
Structured query language (SQL) is a programming language for storing and processing information in a relational database. A relational database stores information in tabular form,
with rows and columns representing differentdata attributes and the various relationships between the data values.SQL statements are used to store, update, remove, search, and retrieve information from the database.It is also used to maintain and optimize database performance.
SQL is a popular query language that is frequently used in all types of applications. Data analysts and developers learn and use SQL because it integrates well with different programming languages. For exampleSQL queries can be embeded with the Java programming language to build high-performing data processing applications with major SQL database systems such as Oracle or MS SQL Server. SQL  uses common English keywords in its statements.

### History of SQL
SQL was invented in the 1970s based on the relational data model. It was initially known as the structured English query language (SEQUEL). The term was later shortened to SQL. Oracle, formerly known as Relational Software,became the first vendor to offer a commercial SQL relational database management system.

### Importance of SQL in data management and business
SQL is crucial in data management and analysis. It serves as a powerful tool for accessing, manipulating, and managing data in relational databases, which are widely used in various industries to store and 
organize information. 

**Universality:** SQL is the standard language for dealing with relational databases.It is compatible with numerous database management systems such as MySQL, SQL Server, Oracle, and PostgreSQL.
This wide applicability makes SQL an essential skill for data professionals.

**Ease of use:** SQL is a relatively easy-to-learn language with a simple, human-readable syntax. It allows users to perform complex data operations without requiring extensive programming knowledge,
making it accessible to a broader range of individuals.

**Efficient data retrieval:** SQL enables  to filter and retrieve specific data from large databases quickly.We can select, sort, and aggregate data based on specific criteria, which is particularly useful in business settings for generating reports, insights, and making data-driven decisions.

**Data manipulation:** SQL allows to easily insert, update, and delete data in a database. This capability is vital for maintaining and managing data, ensuring that the information remains up-to-date and accurate.

**Data integrity and security:** With SQL, We can enforce data integrity rules and constraints, ensuring that the data stored in the database is consistent and reliable. Additionally, SQL provides mechanisms for securing data, such as granting or revoking access permissions to different users, which is essential for safeguarding sensitive information.

### Basic SQL terminology 
Before diving into SQL queries, it’s important to understand the basic terminology used when working with databases and SQL.

**1.Database**
A **database** is a collection of data that is organized in a structured way, usually into tables. It is the environment where all the data is stored, managed, and manipulated. A database can contain one or
more **tables**, which are the fundamental units of data storage.

Example:  
- A company may have a **"company_database"** that contains tables for employees, customers, sales transactions, etc.

**2.Table**
A **table** is a collection of related data stored in rows and columns. Tables are the fundamental building blocks of a database and are used to store the actual data. Each table typically represents a specific entity or subject, such as **employees**, **customers**, or **orders**.

Example:  
- An **"employees"** table may store data about each employee such as their name, job title, salary, etc.

**3.Row**
A **row** (also known as a **record** or **tuple**) is a single, horizontal unit of data in a table. Each row represents a unique entity or instance of the data, and it contains values for each column of the table.

Example:  
- A row in the **"employees"** table could represent a single employee, such as:
  - `EmployeeID = 101`
  - `Name = John Doe`
  - `JobTitle = Software Engineer`
  - `Salary = 80000`

**4.Column**
A **column** (also called an **attribute**) is a vertical unit in a table that contains a specific type of data. Each column has a name and stores data of a specific datatype (e.g., integer, string, date).

Example:  
- A column in the **"employees"** table could be **"Name"**, **"Salary"**, or **"JobTitle"**, where each column stores specific data for each employee.

**5.Field**
A **field** is the intersection of a row and a column in a table. It is the individual value stored at that position. In the **"employees"** table, a field could be something like **John Doe** in the **Name** column, or **80000** in the **Salary** column for a specific employee.

Example:
- For the row representing employee `John Doe`, the value in the **Name** column would be `John Doe`, and the value in the **Salary** column would be `80000`.

**6.Primary Key**
A **primary key** is a column or a set of columns that uniquely identifies each row in a table. No two rows can have the same value in the primary key column(s). This ensures that each record in the table is unique.

Example:  
- In the **"employees"** table, the **EmployeeID** column might be the primary key because each employee has a unique ID.

**7.Foreign Key**
A **foreign key** is a column or a set of columns in one table that refers to the primary key in another table. It establishes a relationship between two tables, allowing them to be linked together.

Example:  
- In a **"sales"** table, there might be a **"EmployeeID"** column, which is a foreign key that links each sale to the specific employee (from the **"employees"** table) who made the sale.

**8.Index**
An **index** is a data structure that improves the speed of data retrieval operations on a table at the cost of additional space and time required to maintain it. Indexes are created on columns that are frequently searched or used in joins.

Example:  
- You may create an index on the **"EmployeeID"** column in the **"employees"** table to speed up searches and queries that use the employee ID.

**9.Query**
A **query** is a request for data or information from a database. SQL queries are used to retrieve, update, insert, and delete data from tables. The most common query is the `SELECT` query, which is used to retrieve data.

Example:  
- A simple query like:
  SELECT Name, JobTitle FROM employees WHERE Salary > 50000;
