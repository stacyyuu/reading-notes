## Readings: Mongo and Mongoose 

### Our reading today is based on NoSQL vs SQL. 
---

## NoSQL vs SQL 

Fill in the chart below with five differences between SQL and NoSQL databases:

| SQL |	NoSQL |
| :---: | :---: |
|  Primarly called Relational Databases (RDBMS)| Primarly called non-relational or distributed database        |
|  Table based databases   |   Document based, key-value pairs, graph databases or wide-column stores which do not have standard schema definitions     |
|   Vertically scalable  |   Horizontally scalable    |
|   Uses SQL (standard query language) for defining and manipulating data  |    Queries are focused on collection of documents, sometimes called UnQL (unstructured query language)    |
|   Ex: MySql, Oracle, Sqlite        |    Ex: MongoDB, BigTable, Redis       |
 	
 	 
1. What kind of data is a good fit for an SQL database?
- These databases are a good for the complex query intensive environment. 
- NoSQL don't have standard interfaces to perform complex queries. 

2. Give a real world example.
- MySQL database: very popular open-source database. 
- By replicating MySQL database across multiple nodes the work load can be reduced heavily, increasing the scalability and availability of business application. 

3. What kind of data is a good fit a NoSQL database?
- Fits better for hierarchial data storage as it follows the key-value pair way of storing data similar to JSON data. 
- Highly preferred for large data set. 

4. Give a real world example.
- MongoDB: one of the most popular document based NoSQL database as it stores data in JSON like documents. 
- For simple queries, it gives good performance, as all the related data is in a single document which eliminates the join operations. 

5. Which type of database is best for hierarchical data storage?
- NoSQL

6. Which type of database is best for scalability?
- In most situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server.
- NoSQL databases are horizontally scalable. You can just add a few more servers easily in your NoSQL database infrastructure to handle the large traffic. 

- For high transactional based apps: SQL databases are best fit for heavy duty transactional type apps, as it is more stable and promises the atomicity as well as integrity of data. 
- For support: Execellent support is available for all SQL databases from their vendors. 
- For properties: SQL databases emphasizes on ACID properties whereas the NoSQL databases follows the Brewers CAP theorem. 
- For DB types: On a high-level, we can classify SQL databases as either open-source or close-sourced from commercial vendors. NoSQL databases can be classified on the basis way of storing data as graph databases, key-value store, document store, column store, and XML store. 

## SQL vs NoSQL continued

1. What does SQL stand for?
- Structured Query Language. 
- SELECT and FROM keywords. 
- SELECT id, name, price FROM products with data/parameters. 

2. What is a relational database?
- Works with certain assumptions or in a certain way and supports the SQL language. 

3. What type of structure does a relational database work with?
- Tables: storage container. 

4. What is a ‘schema’?
- Very strict requirements for data that is stored in database. 
- Clear schema of which data can go into a table.
- Defined by fields (data/parameters), which is the columns. 
- Every new entry or record added is a row. These will have values for our fields.
- Cannot have more fields than the one defined for the  unless another field is added. 
- Typically work with multiple tables that can be connected with relations (JOIN).

5. What is a NoSQL database?
- Build to store lots and lots of data in a very proficient way. 

6. How does it work?
- Has databases that uses collections, similar to tables. 
- Documents, similar to rows. That look like JSON data and don't follow a schema. It can have multiple documents in a collection that has different fields. This doesn't ensure that your data will format how you want it. 
- A more flexible solution where you can store useful data for you to view. 
- In general, no relations. It is possible to relate data, but it is done manually. 
- Instead, the idea is that you put all the information in one place. 
- Less relation merging and super fast and efficient queries. 

7. What is inside of a Mongo database?
- Collections of documents. 

8. Which is more flexible - SQL or MongoDB? and why.
- MongDB since it does not follow schemas. 

9. What is the disadvantage of a NoSQL database?
- Disadvantages are if you have duplicate data, if something changes, you have to update it in multiple collections. 
- Good for data that requires a lot of read and not much write. 

[Back to main page](README.md)
