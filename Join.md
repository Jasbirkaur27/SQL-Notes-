## Introduction to Joins
JOIN is used to combine rows from two or more tables based on a related column. It allows  to retrieve data from multiple tables in a single query, helping to create more meaningful and complex results. The different types of SQL joins specify how rows from the two tables should be matched.<br>
<br>
There are several types of joins in SQL:

**INNER JOIN<br>
LEFT JOIN (or LEFT OUTER JOIN)<br>
RIGHT JOIN (or RIGHT OUTER JOIN)<br>
FULL OUTER JOIN**<br>

### 1. INNER JOIN<br>
An INNER JOIN returns only the rows where there is a match in both tables. If a row in one table does not have a corresponding match in the other table, it will not be included in the result.

Syntax:<br>
<code>
SELECT columns
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;</code><br>
Example:<br>
Suppose you have two tables, employees and departments, and you want to retrieve a list of employees along with their department name.<br>
<code>
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments
ON employees.department_id = departments.department_id;</code><br>
This query will return only those employees who are assigned to a department.<br>

### 2. LEFT JOIN (or LEFT OUTER JOIN)<br>
A LEFT JOIN returns all rows from the left table (the first table), and the matched rows from the right table (the second table). If there is no match, NULL values will be returned for columns from the right table.<br>

Syntax:<br>
<code>
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;</code><br><br>
Example:<br>
Using the employees and departments example, if you want to list all employees even if they are not assigned to any department, you can use a LEFT JOIN.<br>
<code>SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments
ON employees.department_id = departments.department_id;</code><br>
This will return all employees, including those without a department, with NULL in the department_name column for those without a match.<br>

### 3. RIGHT JOIN (or RIGHT OUTER JOIN)<br>
A RIGHT JOIN is the opposite of the LEFT JOIN. It returns all rows from the right table, and the matched rows from the left table. If there is no match, NULL values will be returned for columns from the left table.<br>

Syntax:<br>
<code>SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.common_column = table2.common_column;</code><br><br>
Example:<br>
If you want to list all departments and their employees (including departments with no employees), you can use a RIGHT JOIN:<br>
<code>SELECT employees.name, departments.department_name
FROM employees
RIGHT JOIN departments
ON employees.department_id = departments.department_id;</code><br>
This will return all departments, even those with no employees, showing NULL for the employee name where applicable.<br><br>

**4. FULL OUTER JOIN**<br>
A FULL OUTER JOIN returns all rows when there is a match in one of the tables. It returns NULL for non-matching rows in either table. It’s essentially a combination of a LEFT JOIN and a RIGHT JOIN.<br>

Syntax:<br>

<code>SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.common_column = table2.common_column;</code><br><br>
Example:<br>
If you want to list all employees and all departments, whether or not they have matches, you can use a FULL OUTER JOIN:<br>
<code>SELECT employees.name, departments.department_name
FROM employees
FULL OUTER JOIN departments
ON employees.department_id = departments.department_id;</code><br>
This will return all employees and all departments, showing NULL where there is no corresponding match in the other table.<br>

**How to Combine Data from Multiple Tables Using JOIN**
To combine data from multiple tables, you must have a common column in the tables you want to join. The most common practice is to join tables using primary key and foreign key relationships. 
For example:<br>

customers table might have a customer_id as the primary key.
orders table might have customer_id as a foreign key linking back to the customers table.
You can combine them using a JOIN like this:<br>
<code>SELECT customers.name, orders.order_date
FROM customers
JOIN orders
ON customers.customer_id = orders.customer_id;</code><br>
This will return the name of the customer along with the order date for each order in the orders table.<br>


