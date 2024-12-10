### UNION, INTERSECT, and EXCEPT: Combining Result Sets in SQL
In SQL, the UNION, INTERSECT, and EXCEPT operators are used to combine or compare result sets from two or more queries. 

**1. UNION**<br>
The UNION operator combines the result sets of two or more SELECT queries. It returns all unique rows from each query. If there are duplicate rows between the queries, UNION automatically removes them.

Syntax:<br>
<code>SELECT column1, column2, ...
FROM table1
UNION
SELECT column1, column2, ...
FROM table2;</code><br>
Key Points:<br>
Returns all unique rows (no duplicates).<br>
The number and order of columns in each SELECT query must be the same.<br>
It is slower than UNION ALL since it checks for duplicates.<br>
Example:<br>

<code>SELECT name FROM employees
UNION
SELECT name FROM contractors;</code><br>
This query combines the names of employees and contractors, but if any names are repeated in both result sets, they will appear only once in the final output.<br>
<br>
**2. INTERSECT**<br>
The INTERSECT operator returns only the rows that are common to the result sets of two SELECT queries. In other words, it will give you the intersection of the two result sets.
<br>
Syntax:
<br>
<code>SELECT column1, column2, ...
FROM table1
INTERSECT
SELECT column1, column2, ...
FROM table2;</code><br>
Key Points:<br>
Returns only the rows that exist in both result sets.<br>
The number and order of columns in each SELECT query must be the same.<br>
If there are no common rows, the result will be an empty set.<br>
Example:
<br>
<code>SELECT name FROM employees
INTERSECT
SELECT name FROM contractors;</code><br>
This query will return only the names that are present in both the employees and contractors tables.
<br><br>
**3. EXCEPT**<br>
The EXCEPT operator returns the rows from the first SELECT query that do not exist in the second SELECT query. It gives the difference between the two result sets.
<br>
Syntax:
<br>
<code>SELECT column1, column2, ...
FROM table1
EXCEPT
SELECT column1, column2, ...
FROM table2;</code><br>
Key Points:<br>
Returns rows from the first query that do not exist in the second query.<br>
The number and order of columns in each SELECT query must be the same.<br>
If there are no unique rows in the first result set, the result will be empty.<br>
Example:<br>
<code>SELECT name FROM employees
EXCEPT
SELECT name FROM contractors;</code><br>
This query will return the names that are only in the employees table and not in the contractors table.<br><br>
**4. Differences Between UNION and JOIN**<br>
Although both UNION and JOIN are used to combine data from multiple tables, they serve different purposes and work in distinct ways:
<br>
Feature	UNION	JOIN<br>
Purpose	Combines result sets from multiple queries	Combines columns from multiple tables based on related keys<br>
Operation	Stacks rows on top of each other (union of results)	Merges columns horizontally based on a condition (e.g., ON clause)<br>
Handling Duplicates	Removes duplicates (unless UNION ALL)	No automatic duplicate removal (can be controlled with DISTINCT)<br>
Number of Columns	Must be the same in both SELECT queries	Can combine different numbers of columns from each table<br>
Use Case	Use when you want to combine data vertically (same data from different sources)	Use when you need to combine related data horizontally (like joining customer info with order details)<br>
Example of JOIN:<br>
<code>SELECT employees.name, contractors.name
FROM employees
JOIN contractors
ON employees.department = contractors.department;</code><br>
This JOIN query combines rows from the employees and contractors tables where the department matches.<br>

Example of UNION:<br>
<code>SELECT name FROM employees
UNION
SELECT name FROM contractors;</code><br>
This UNION query combines the name columns from both tables and eliminates duplicates.<br>



