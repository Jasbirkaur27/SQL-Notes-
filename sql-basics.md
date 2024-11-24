## SQL Basics
To do some operations on the data in the database, then you must have to write the query in the predefined syntax of SQL.<br>
The syntax of the structured query language is a unique set of rules and guidelines, which is not case-sensitive. Its Syntax is defined and maintained by the ISO and ANSI standards.<br>
**Following are some most important points about the SQL syntax which are to remember:**<br>
1.SQL Queries can be written both in uppercase and lowercase but uppercase improves the readability of the SQL query.<br>
2.SQL statements or syntax are dependent on text lines. We can place a single SQL statement on one or multiple text lines.<br>

## SQL Statement
SQL statements tell the database what operation you want to perform on the structured data and what information you would like to access from the database.
The statements of SQL are very simple and easy to use and understand. They are like plain English but with a particular syntax.

Each SQL statement begins with any of the SQL keywords and ends with the semicolon (;).
The semicolon is used in the SQL for separating the multiple Sql statements which are going to execute in the same call.

## Types of Commands 
SQL statements have different commands. types of Commands are :<br>
![image](https://github.com/user-attachments/assets/251837a3-ecff-42c0-852c-6b26836e6a98)
<br>
### 1.Data Definition Language
DDL or Data Definition Language actually consists of the SQL commands that can be used for defining, altering, and deleting database structures such as tables, indexes, and schemas. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.<br>
**DDL Commands are:**
<br>
1.create: used to create a table.   Syntax : CREATE TABLE table_name(column1 data_type, column2 data_type, ...);<br>
2.DROP: It is used to delete the table.      syntax: DROP TABLE table_name;<br>
3.ALTER: Alter the structure of the database Syntax: ALTER TABLE table_name ADD COLUMN column_name data_type;<br>
4.TRUNCATE: Remove all records from a table, including all spaces allocated for the records are removed	Syntax: TRUNCATE TABLE table_name;<br>
5.RENAME: Rename an object existing in the database	Syntax: RENAME TABLE old_table_name TO new_table_name;<br>

### 2.Data Manipulation Language (DML)
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.<br>
**Common DML Commands:**
<br>
1.INSERT: Insert data into a table.             Syntax: INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);<br>
2.UPDATE:	Update existing data within a table.  Syntax: UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;<br>
3.DELETE:	Delete records from a database table. Syntax:	DELETE FROM table_name WHERE condition;<br>

### Data Control Language (DCL)
DCL (Data Control Language) includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system. These commands are used to control access to data in the database by granting or revoking permissions.<br>
**Common DCL Commands**<br>
1.GRANT:	Assigns new privileges to a user account, allowing access to specific database objects, actions, or functions. Syntax: GRANT privilege_type [(column_list)] ON [object_type] object_name TO user [WITH GRANT OPTION];<br>
2.REVOKE: Removes previously granted privileges from a user account, taking away their access to certain database objects or actions.	REVOKE [GRANT OPTION FOR] privilege_type [(column_list)] ON [object_type] object_name FROM user [CASCADE];

### Transaction Control Language (TCL)
Transactions group a set of tasks into a single execution unit. Each transaction begins with a specific task and ends when all the tasks in the group are successfully completed. If any of the tasks fail, the transaction fails. Therefore, a transaction has only two results: success or failure. We can explore more about transactions here.<br>
**Common TCL Commands**<br>
1.BEGIN: TRANSACTION	Starts a new transaction. Syntax:BEGIN TRANSACTION [transaction_name];<br>
2.COMMIT: Saves all changes made during the transaction. Synatx: COMMIT;<br>
3.ROLLBACK:	Undoes all changes made during the transaction. Synatx:ROLLBACK;<br>
4.SAVEPOINT: Creates a savepoint within the current transaction. Synatx:SAVEPOINT savepoint_name;<br>



Resources: Geeksforgeeks, Javatpoint,W3school
