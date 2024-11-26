# CREATE STATEMENT
The create command is used to create a table. <br>
Syntax:<br>
<code>CREATE table table_name<br>
(<br>
Column1 datatype (size),<br>
column2 datatype (size),<br>
.<br>
.<br>
columnN datatype(size)<br>
);
 </code><br>
table_name: The name you assign to the new table.<br>
column1, column2, … : The names of the columns in the table.<br>
datatype(size): Defines the data type and size of each column.<br>

# INSERT STATEMENT
The insert command is used to insert values in table.<br>
syntax:<br>
INSERT INTO table_name (column1, column2, …) VALUES (value1, value2, …);<br>


# SELECT STATEMENT 
The select query in SQL is one of the most commonly used SQL commands to retrieve data from a database. With the select command in SQL, users can access data and retrieve specific records based on various conditions, making it an essential tool for managing and analyzing data.
We can fetch either the entire table or according to some specified rules. The data returned is stored in a result table.<br>

### Syntax :
<code> SELECT * from TABLE_NAME; </code><br>
This code is used to fetch the whole table. To fetch some columns the syntax is :<br>
<code> SELECT column1,column2…. FROM table_name ;</code><br>


### Example <br>
**CREATE TABLE:**<br>
CREATE TABLE Customer(<br>
    CustomerID INT PRIMARY KEY,<br>
    CustomerName VARCHAR(50),<br>
    LastName VARCHAR(50),<br>
    Country VARCHAR(50),<br>
    Age int(2),<br>
  Phone int(10)<br>
);<br>
**-- Insert some sample data into the Customers table**<br>
INSERT INTO Customer (CustomerID, CustomerName, LastName, Country, Age, Phone)<br>
VALUES (1, 'Shubham', 'Thakur', 'India','23','xxxxxxxxxx'),<br>
       (2, 'Aman ', 'Chopra', 'Australia','21','xxxxxxxxxx'),<br>
       (3, 'Naveen', 'Tulasi', 'Sri lanka','24','xxxxxxxxxx'),<br>
       (4, 'Aditya', 'Arpan', 'Austria','21','xxxxxxxxxx'),<br>
       (5, 'Nishant. Salchichas S.A.', 'Jain', 'Spain','22','xxxxxxxxxx');<br>
**Retrieve Data using SELECT Query** <br>
<code>SELECT CustomerName, LastName FROM Customer;     </code>  
Output: <br>
![image](https://github.com/user-attachments/assets/459f91b6-9111-453a-b1cc-8f8c4261401b)
<br>
**Fetch All Table using SELECT Statement**<br>
<code>SELECT * FROM Customer;</code>
Output:<br>
![image](https://github.com/user-attachments/assets/30eeb5f7-6b42-4f8f-a646-a4b4b3d3ca7e)


