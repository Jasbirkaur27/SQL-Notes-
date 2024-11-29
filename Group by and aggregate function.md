### GROUP BY 
The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country".<br>

The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.<br>
Syntax:<br>
<code>SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s);</code>
<br>
Example:<br>
<code>SELECT Country,COUNT(CustomerID) as total
FROM Customers
GROUP BY Country;</code><br>
This example has grouped data according to coutries and will give us Country and total customers in each country in  total column.<br>
### Aggregate Functions
**1.COUNT()**<br>
The COUNT() function returns the number of rows that match a specified condition.<br>
Syntax:<br>
<code>SELECT COUNT(column_name) FROM table_name;</code><br>
Example:
<code>SELECT COUNT(*) FROM employees;</code><br>
This returns the total number of rows in the employees table.<br>

**2.SUM()**<br>
The SUM() function calculates the total sum of a numeric column.<br>
Syntax:<br>
<code>SELECT SUM(column_name) FROM table_name;</code><br>
Example:<br>
<code>SELECT SUM(salary) FROM employees;</code><br>
This returns the total salary paid to employees.<br>

**3.AVG()**<br>
The AVG() function calculates the average value of a numeric column.<br>
Syntax:<br>
<code>SELECT AVG(column_name) FROM table_name;</code><br>
Example:<br>
<code>SELECT AVG(salary) FROM employees;</code><br>
This returns the average salary of employees.<br>

**4 MIN() and MAX()**<br>
The MIN() and MAX() functions return the minimum and maximum values from a specified column.<br>
Syntax:<br>
<code>SELECT MIN(column_name), MAX(column_name) FROM table_name;</code><br>
Example:<br>
<code>SELECT MIN(salary), MAX(salary) FROM employees;</code><br>
This returns the lowest and highest salaries in the employees table.<br>

### HAVING Clause<br>
The HAVING clause is used to filter groups based on a condition, similar to how the WHERE clause filters individual rows. However, HAVING is used with aggregate functions, whereas WHERE is used to filter rows before grouping.<br>
Syntax:<br>
<code>SELECT column1, aggregate_function(column2)
FROM table_name
GROUP BY column1
HAVING condition;</code><br>
Explanation:<br>
condition: The condition to filter groups (typically using aggregate functions).<br>
Example:<br>
<code>SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;</code><br>
This query groups employees by department and calculates the average salary. It then filters the result to only include departments where the average salary is greater than 50,000.<br>
