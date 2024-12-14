## SQL Joins 
we store our data in multiple logical tables that are linked together by a common key value in relational databases.As a result, we constantly need to get data from two or more tables into the desired output based on some conditions. We can quickly achieve this type of data in SQL Server using the SQL JOIN clause.<br>

<br>In a JOIN query, a condition indicates how two tables are related:<br>
Choose columns from each table that should be used in the join. A join condition indicates a foreign key from one table and its corresponding key in the other table.<br>
Specify the logical operator to compare values from the columns like =, <, or >.<br>
### SELF JOIN
A table is joined to itself using the SELF JOIN. It means that each table row is combined with itself and with every other table row. The SELF JOIN can be thought of as a JOIN of two copies of the same tables. We can do this with the help of table name aliases to assign a specific name to each table's instance. The table aliases enable us to use the table's temporary name that we are going to use in the query. It's a useful way to extract hierarchical data and comparing rows inside a single table.<br>
It works the same as the syntax of joining two different tables.we use aliases names for tables because both the table name are the same.<br>
<code>SELECT T1.col_name, T2.col_name...    
FROM table1 T1, table1 T2    
WHERE join_condition;    </code><br>
**Example using self join**<br>
<code>SELECT S1.first_name, S2.last_name, S2.city  
FROM Student S1, Student S2  
WHERE S1.id <> S2.iD AND S1.city = S2.city  
ORDER BY S2.city;  </code>
### CROSS JOIN
CROSS JOIN in SQL Server combines all of the possibilities of two or more tables and returns a result that includes every row from all contributing tables. It's also known as CARTESIAN JOIN because it produces the Cartesian product of all linked tables. The Cartesian product represents all rows present in the first table multiplied by all rows present in the second table.<br>
<br>
**Syntax:**<br>
<code>SELECT column_lists    
FROM table1    
CROSS JOIN table2;  </code><br>
**Example:**<br>
<code>SELECT Student.admission_no, Student.first_name, Student.last_name, Fee.course, Fee.amount_paid  
FROM Student  
CROSS JOIN Fee  
WHERE Student.admission_no = Fee.admission_no;  </code><br>

