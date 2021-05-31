# Readings: Mongo and Mongoose

[SQL vs NoSQL Database](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

   
|   SQL                                  |   NoSQL                                         |
| ---------------------------------------|-------------------------------------------------|
|Relational Databases (RDBMS             |non-relational or distributed database.          |
|                                        |                                                 |
|   are table based databases            |document based, key-value pairs,                 |
|                                        | graph databases or wide-column stores           |
|vertically scalable                     |horizontally scalable                            |
|uses( structured query language ),      | (Unstructured Query Language).                  |
|for defining and manipulating the data  | are focused on collection of documents          |
| examples: MySql, Oracle, Sqlite        |MongoDB, BigTable, Redis, RavenDbNeo4j, Cassandra|
|fit complex query intensive environment |not good fit for complex queries.                |
|not best for hierarchical data storage. |better for the hierarchical data storage         |
|Best for heavy duty transactional apps  | not comparable and sable enough with that type  |

 	 	 
1. **What kind of data is a good fit for an SQL database?**
fit complex query intensive environment and heavy duty transactional apps 
2. **Give a real world example.**
SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL.

3. **What kind of data is a good fit a NoSQL database?**
hierarchical data storage

4. **Give a real world example.**
 NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb

5. **Which type of database is best for hierarchical data storage?**
NoSQL

6. **Which type of database is best for scalability?**
SQL 

<!-- Bookmark
[mongoose api](https://mongoosejs.com/docs/api.html#Model) -->
----
[Sql vs NoSql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

1. **What does SQL stand for?**  
structured query language

2. **What is a realational database?**
consists of a collection of tables, each having a unique name.
works in a certian way 

3. **What type of structure does a relational database work with?**
tabels 

4. **What is a ‘schema’?** 
design that represents the storage of your data(as a blueprint ) in a database

5. **What is a NoSQL database?**
are document-oriented NoSQL databases
that stores a data in very efficient way

6. **How does it work?**
stores data in collections that has a document(like rows) inside it 

7. **What is inside of a Mongo database?**
collections and documents

8. **Which is more flexible - SQL or MongoDB? and why.**
MONODB because it is no schema relied, so it order data with key and value
which is faster

9. **What is the disadvantage of a NoSQL database?**
you have some duplicated data
if the product name changs you have to update everything