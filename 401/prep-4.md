## Relational Databases and SQL

- **SQL** or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. Due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications. 
- Many popular SQL databases include SQLite, MySQL, Postgres, Oracle, and Microsoft SQL Server. 
- A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (attributes or properties of the table) and any number of rows of data. 
<br>
<br>
- To retrieve data from a SQL database, we need to write **SELECT** statements, which are often referred to as **queries**. A query itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has specific syntax. 
- Select query for a specific column <br>
SELECT column, another_column, … <br>
FROM mytable;
- Select query for all columns <br>
SELECT * <br>
FROM mytable;

<br>
<br>

- In order to filter certain results from being returned, we need to use a **WHERE** clause in query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not. 
- Select query with constraints<br>
SELECT column, another_column, … <br>
FROM mytable<br>
WHERE condition<br>
    AND/OR another_condition<br>
    AND/OR …;

| Operator	| Condition	 | SQL Example |
| :---: | :---: | :---:|
|=, !=, < <=, >, >=	| Standard numerical operators	| col_name != 4 |
BETWEEN … AND …	| Number is within range of two values (inclusive)	|col_name **BETWEEN** 1.5 **AND** 10.5 |
NOT BETWEEN … AND …	| Number is not within range of two values (inclusive) |	col_name **NOT BETWEEN** 1 **AND** 10 |
IN (…)	| Number exists in a list	| col_name **IN** (2, 4, 6) |
NOT IN (…)	| Number does not exist in a list	| col_name **NOT IN** (1, 3, 5)

<br>
<br>

- When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching.


| Operator	| Condition	 | Example |
| :---: | :---: | :---:|
=	 | Case sensitive exact string comparison (**notice the single equals**)	| col_name = "abc"
!= or <>	| Case sensitive exact string inequality comparison	| col_name **!**= "abcd"
LIKE	| Case insensitive exact string comparison	| col_name **LIKE** "ABC"
NOT LIKE	| Case insensitive exact string inequality comparison	| col_name **NOT LIKE** "ABCD"
%	| Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	| col_name **LIKE** "%AT%"(matches "AT", "ATTIC", "CAT" or even "BATS")
_	| Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)	| col_name **LIKE** "AN_"(matches "AND", but not "AN")
IN (…)	| String exists in a list	| col_name **IN** ("A", "B", "C")
NOT IN (…)	| String does not exist in a list	| col_name **NOT IN** ("D", "E", "F")

- SQL provides a convenient way to discard rows that have a duplicate column value by using the **DISTINCT** keyword. 
- Select query with unique results <br>
SELECT DISTINCT column, another_column, … <br>
FROM mytable <br>
WHERE condition(s);
- Since the DISTINCT keyword will blindly remove duplicate rows, we will learn in a future lesson how to discard duplicates based on specific columns using grouping and the **GROUP BY** clause. 

<br>
<br>

- SQL provides a way to sort your results by a given column in ascending or descending order using the **ORDER BY** clause. 
- Select query with ordered results <br>
SELECT column, another_column, … <br>
FROM mytable <br> 
WHERE condition(s) <br>
ORDER BY column ASC/DESC;
- When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text. 

<br>
<br>

- Another clause which is commonly used with the ORDER BY clause are the **LIMIT** and **OFFSET** clauses, which are a useful optimization to indicate to the database the subset of the results you care about. 
- The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.
- Select query with limited rows <br>
SELECT column, another_column, … <br>
FROM mytable <br>
WHERE condition(s) <br>
ORDER BY column ASC/DESC <br>
LIMIT num_limit OFFSET num_offset; <br>

<br>
<br>

- Database normalization is useful because it minimizes duplicate data in any single table, and allows for data in database to grow independently of each other. 
- As a trade off, queries get slightly more complex since they have to be able to find data from different parts of the database, and performance issues can arise when working with many large tables. 
- Tables that share information about a single entity need to have a *primary key* that identifies that entity *uniquely* across the database. One common primary key type is an auto-incrementing integer (because they are space efficient), but it can also be a string, hashed value, so long as it's unique. 
- Using the **JOIN** clause in a query, we can combine row data across two separate tables using this unique key. The first of the joins we will introduce is the **INNER JOIN**.
- Select query with INNER JOIN on multiple tables <br>
SELECT column, another_table_column, … <br>
FROM mytable <br>
INNER JOIN another_table <br> 
    ON mytable.id = another_table.id <br>
WHERE condition(s) <br>
ORDER BY column, … ASC/DESC <br>
LIMIT num_limit OFFSET num_offset;
- The **INNER JOIN** is a process that matches rows from the first table and the second which have the same key (as defined by the **ON** constraint) to create a result row with the combined columns from both tables. 
- After the tables are joined, the other clauses we learned previously are then applied. 

<br>
<br>

- The **database schema** is what describes the structure of each table and the datatypes that each column of the table can contain. 
- Use the **INSERT** statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert. 
- In general, each row of data you insert should contain values for every corresponding column in the table. You can insert multiple rows a time by just listing them sequentially. 
- Insert statement with values for all columns <br>
INSERT INTO mytable <br>
VALUES (value_or_expr, another_value_or_expr, …), <br>
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
- In some cases, if you have incomplete data and the table contains columns that support default values, you can insert rows with only the columns of data you have by specifying them explicity. 
- Insert statement with specific columns <br>
INSERT INTO mytable <br>
(column, another_column, …) <br>
VALUES (value_or_expr, another_value_or_expr, …), <br>
      (value_or_expr_2, another_value_or_expr_2, …),
      …;
- In these cases, the number of values need to match the number of columns specified. 
- Example Insert statement with expressions <br>
INSERT INTO boxoffice <br>
(movie_id, rating, sales_in_millions) <br>
VALUES (1, 9.9, 283742034 / 1000000);

<br> 
<br>

- Another common task includes updating existing data, this can be done using the **UPDATE** statement. Similar to INSERT, you have to specify exactly which table, columns, and rows to update. 
- Update statement with values <br>
UPDATE mytable <br> 
SET column = value_or_expr, <br> 
    other_column = another_value_or_expr, <br>
    … <br>
WHERE condition;
- This applies changes to each and every row that satisfies the contraint in the WHERE clause. 
- Without the WHERE clause, the updates will apply to all rows. 
- One helpful tip is to write the constraint first and test it in a SELECT query to make sure the right rows are being updated. 

<br>
<br>

- **DELETE** statement is used to delete data from a table in the database. Make sure to include the WHERE clause. 
- Delete statement with condition <br>
DELETE FROM mytable <br>
WHERE condition;

<BR>
<BR>

- You can create a new database table using the **CREATE TABLE** statement. 
- Create table statement w/ optional table constraint and default value <br>
CREATE TABLE IF NOT EXISTS mytable ( <br>
    column DataType TableConstraint DEFAULT default_value, <br>
    another_column DataType TableConstraint DEFAULT default_value,
    … <br>
); 


| Data type |	Description|
| :---: | :---: |
INTEGER, BOOLEAN |	The integer datatypes can store whole integer values like the count of a number or an age. In some implementations, the boolean value is just represented as an integer value of just 0 or 1.
FLOAT, DOUBLE, REAL	| The floating point datatypes can store more precise numerical data like measurements or fractional values. Different types can be used depending on the floating point precision required for that value.
CHARACTER(num_chars), VARCHAR(num_chars), TEXT	| The text based datatypes can store strings and text in all sorts of locales. The distinction between the various types generally amount to underlaying efficiency of the database when working with these columns.  <br> Both the CHARACTER and VARCHAR (variable character) types are specified with the max number of characters that they can store (longer values may be truncated), so can be more efficient to store and query with big tables.
DATE, DATETIME	| SQL can also store date and time stamps to keep track of time series and event data. They can be tricky to work with especially when manipulating data across timezones.
BLOB	|Finally, SQL can store binary data in blobs right in the database. These values are often opaque to the database, so you usually have to store them with the right metadata to requery them.


Constraint	| Description
| :---: | :---: |
PRIMARY KEY	| This means that the values in this column are unique, and each value can be used to identify a single row in this table.
AUTOINCREMENT	| For integer values, this means that the value is automatically filled in and incremented with each row insertion. Not supported in all databases.
UNIQUE | This means that the values in this column have to be unique, so you can't insert another row with the same value in this column as another row in the table. Differs from the `PRIMARY KEY` in that it doesn't have to be a key for a row in the table.
NOT NULL	| This means that the inserted value can not be `NULL`.
CHECK (expression)	| This allows you to run a more complex expression to test whether the values inserted are valid. For example, you can check that values are positive, or greater than a specific size, or start with a certain prefix, etc.
FOREIGN KEY	| This is a consistency check which ensures that each value in this column corresponds to another value in a column in another table. <br> For example, if there are two tables, one listing all Employees by ID, and another listing their payroll information, the `FOREIGN KEY` can ensure that every row in the payroll table corresponds to a valid employee in the master Employee list.

<br>
<br>

- As data changes over time, you can use the **ALTER TABLE** statement to add, remove, or modify columns, and table constraints. 
- Adding columns: Similar to creating new rows. You can specify where to insert the new column using the **FIRST** or **AFTER** clauses, though this is not a standard feature. 
- Altering table to add new column(s) <br>
ALTER TABLE mytable <br>
ADD column DataType OptionalTableConstraint  <br>
    DEFAULT default_value;
- Removing columns: 
- Altering table to remove column(s) <br>
ALTER TABLE mytable <br>
DROP column_to_be_deleted;
- Renaming the table: you can use the **RENAME TO** clause. 
- Altering table name <br> 
ALTER TABLE mytable <br>
RENAME TO new_table_name;

<br>
<br>

- In cases you want to remove an entire table including all of its data, you can use the **DROP TABLE** statement, which differs from DELETE because it removes the table schema from the database entirely. 
- Drop table statement <br>
DROP TABLE IF EXISTS mytable;

## SQL Lessons 1-6, 13-18

<img src = "img/SQL 1.png">
<img src = "img/SQL 2.png">
<img src = "img/SQL 3.png">
<img src = "img/SQL 4.png">
<img src = "img/SQL 5.png">
<img src = "img/SQL 6.png">
<img src = "img/SQL 13.png">
<img src = "img/SQL 14.png">
<img src = "img/SQL 15.png">
<img src = "img/SQL 16.png">
<img src = "img/SQL 17.png">
<img src = "img/SQL 18.png">

[Back to main page](README.md)