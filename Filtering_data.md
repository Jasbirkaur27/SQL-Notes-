## Filtering data
Filtering data in SQL is crucial for refining and narrowing down the information retrieved from a database using SELECT. The DISTINCT command is one of the primary tools in SQL for eliminating duplicate records and ensuring that only unique data is returned.Filtering data involves specifying conditions in a query that limit which rows are returned. This is done using the WHERE clause, which enables users to apply conditions based on specific criteria (e.g., a particular value in a column, a range of values, or a relationship between columns).<br>
### DISTINCT <br>
The DISTINCT command in SQL is used to remove duplicate rows from the result set. This command ensures that only unique records are included, which is particularly useful when you're working with data where multiple rows may contain the same information.<br>

Syntax for DISTINCT:
<code>
SELECT DISTINCT column1, column2
FROM table_name;</code><br>
DISTINCT is placed immediately after the SELECT keyword.<br>
It applies to all columns listed in the SELECT statement.<br><br>
**Example** : Consider a table called Orders where customers may place multiple orders on different dates. If we wanted to see a list of unique customer IDs without duplicates:<br>
<code>SELECT DISTINCT customer_id
FROM Orders;</code><br>
This query would return a list of unique customer IDs, even if some customers have placed multiple orders.<br>

### WHERE clause 
The WHERE clause  is used to filter records based on a condition. It limits the rows returned in a query to those that meet the specified criteria.<br>
Syntax:<br>
<code>SELECT column1, column2
FROM table_name
WHERE condition;</code><br>
column1, column2: Specify the columns you want to retrieve data from.<br>
condition: The condition that must be true for a row to be included in the result set.<br><br>
The WHERE clause can filter data based on:<br>
Equality (e.g., =),Inequality (e.g., <>, !=),Range conditions (e.g., BETWEEN, IN),Pattern matching (e.g., LIKE),NULL values (e.g., IS NULL, IS NOT NULL),Comparison operators (e.g., >, <, >=, <=).<br>
<br>** Examples: **<br>
1.<code>SELECT first_name, last_name, department
FROM employees
WHERE department = 'Sales';</code><br>
This query retrieves the first_name, last_name, and department columns from the employees table where the department is 'Sales'.<br><br>
2.<code>SELECT product_name, price
FROM products
WHERE price BETWEEN 10 AND 50;</code><br>
This query retrieves the product_name and price from the products table where the price is between 10 and 50 (inclusive).<br><br>
3.<code>SELECT customer_id, first_name, last_name
FROM customers
WHERE country IN ('USA', 'Canada', 'Mexico');</code><br>
This query retrieves customer details for customers located in 'USA', 'Canada', or 'Mexico'.<br><br>
4.<code>SELECT first_name, last_name
FROM employees
WHERE email IS NULL;</code><br>
This query retrieves employees who do not have an email address (i.e., NULL).<br><br>
5.<code>SELECT first_name, last_name, department, salary
FROM employees
WHERE department = 'Engineering' AND salary > 60000;</code><br>
This query retrieves employees in the 'Engineering' department with a salary greater than 60,000.<br><br>

