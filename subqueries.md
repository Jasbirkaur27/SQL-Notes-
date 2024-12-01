## Introduction to Subqueries
A **subquery** is a query nested inside another SQL query. Subqueries are used to perform operations that require multiple steps in a single query. They can return a single value, a set of values, or even an entire table. Subqueries are commonly used in SELECT, FROM, and WHERE clauses to perform complex filtering, data retrieval, or computation.

### Types of Subqueries:
 **Scalar Subquery**: A scalar subquery returns a single value (one row, one column). It is typically used in expressions like WHERE, HAVING, or SELECT. <br>Example:<br>`SELECT name FROM employees WHERE salary = (SELECT MAX(salary) FROM employees);`

**Inline Subquery**:An inline subquery is used in the FROM clause and acts as a temporary table.This subquery can return multiple rows and columns, and is often used to combine data from multiple tables. Example: <br>
     <code>SELECT subquery.department, AVG(subquery.salary)
     FROM (SELECT department, salary FROM employees) AS subquery
     GROUP BY subquery.department;</code><br><br>
 **Correlated Subquery**: A correlated subquery depends on the outer query for its values.The subquery is executed once for each row of the outer query.<br>Example:<br>
<code>SELECT e.name, e.salary 
     FROM employees e 
     WHERE e.salary > (SELECT AVG(salary) FROM employees WHERE department = e.department);</code>
<br><br>

### Common SQL Clauses for Subqueries
**WHERE Clause:** Filters data based on the subquery results.<br>
**FROM Clause:** Treats the subquery result as a derived table.<br>
**HAVING Clause:** Filters grouped data.<br>

**Subqueries in FROM Clause**
   Subqueries in the FROM clause are often used as derived tables (or inline views).<br>
<code>SELECT department, AVG(salary) FROM 
     (SELECT department, salary FROM employees WHERE salary > 50000) AS high_salary_employees
   GROUP BY department;</code>

**Subqueries in WHERE Clause**
   This is the most common use of subqueries. A subquery in the WHERE clause helps filter results based on values from another query.<br>
   <code>SELECT name FROM employees WHERE department_id IN (SELECT id FROM departments WHERE name = 'Sales');</code>

## Examples

- **Example 1: Scalar Subquery in WHERE Clause**
  <code>SELECT name 
  FROM employees 
  WHERE salary > (SELECT AVG(salary) FROM employees);</code>

- **Example 2: Correlated Subquery**
  <code>SELECT e.name, e.salary 
  FROM employees e 
  WHERE e.salary > (SELECT AVG(salary) FROM employees WHERE department = e.department);</code>

- **Example 3: Inline Subquery in FROM Clause**
  ```
  SELECT department, AVG(salary)
  FROM (SELECT department, salary FROM employees WHERE salary > 40000) AS high_salary_employees
  GROUP BY department;
  ```
