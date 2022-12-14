## Data Modeling

### NoSQL vs SQL

1. What type of database is the best fit for the complex query intensive environment?
- SQL
- NoSQL does not have standard interfaces to perform complex queries and the queries themselves are not as powerful as SQL 

2. What type of database is the best fit for hierarchical data storage?
- NoSQL as it follows the key-value pair way of storing data similar to JSON data
- No SQL are highly preferred for large data set 

3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
- In most situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server.
- NoSQL databases are horizontally scalable. You can just add a few more servers easily in your NoSQL database infrastructure to handle the large traffic. 

### SQL Modeling Techniques

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
- An entry in one table can be related to more than one entry in another, this is called one-to-many relationship 
- The child table has to reference a row on the parent table 
- Add a foreign key constraint on the child table, this indicated that each value stores in this new column references a row on the parent table 
- When you add a row to the child table, the value of the referencing column must match one (and only one) value in the parent table

2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
- Create a diagram of the database tables and their relationships. 
- May be done during design process, as your data modeling, or once the database is created, in order to document the tables' dependencies. 

3. Explain the difference between a primary and foreign key.
- Primary: uniquely identify each row in a table. A table typically has one primary key, but can have more. When the key has more than one column, it is called a compound key. 
- Foreign: a column or set of columns which match a primary key in another table. 

### SQL vs NoSQL 
1. How do we treat keywords and parameters differently in SQL syntax?
- SQL databases are relational and use structured query language with a predefined schema 
- SQL includes SQL keywords

2. Define normalization within the context of schemas and data.
- Organization of data to appear similar across all records and fields, using a set of formal criteria and rules 

3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
- One-to-one: a record in one table is related to one record in another table.
- One-to-many: a record in one table is related to many records in another table.
- Many-to-many: multiple records in one table are related to multiple records in another table. 