
# Reading Notes 11

[Back to the table of contents](../../README.md)

## Reading

Fill in the chart below with five differences between SQL and NoSQL databases:

| SQL                                                                     | NoSQL                                                                                        |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Table Based, each table with n rows of data                             | Document based, using key value pairs with a graph database or wide-column stores            |
| Pre-defined schema                                                      | Dynamic schema                                                                               |
| Scaled vertically, requiring more processing power for bigger databases | Scaled Horizontally, requiring more servers for bigger databases                             |
| Uses SQL calls to access the database                                   | Uses UnQL, or basically no SQL. Has varying ways to access the database between types of dbs |

* What kind of data is a good fit for an SQL database?
  * Complex databases, essentially. SQL calls are really great for navigating it, and tables can be pretty complex.
* Give a real world example.
  * The administration for a server that runs code I've made for it uses an SQL database for tracking banned players. There's a ton of information like what times they were banned, ban reasons, expiration dates, and more that needs to be stored.
* What kind of data is a good fit a NoSQL database?
  * Simpler databases. NoSQL calls are not as powerful, but for small and simple things it is easy to get working. On top of simple databases, huge databases can be a good idea to NoSQL as it is easier to manage the higher cost. More processing power is not ideal.
* Give a real world example.
  * MongoDB, which is as simple as databases get. It holds information in a json-like format, has varying schema, and takes advantage of the good parts of NoSQL.
* Which type of database is best for hierarchical data storage?
  * SQL
* Which type of database is best for scalability?
  * NoSQL

# Video

* What does SQL stand for?
  * Structured Query Language - hoho I already knew that!
* What is a relational database?
  * A database that works with multiple tables that communicate via ids. For example, user table has an ID for a username, and the contact info table may have an id attached to a phone number. The user's ID and a table's ID for a phone number are the same to match up!
* What type of structure does a relational database work with?
  * One to One, One to Many, and Many to Many. One to One points a single user to a single item, One to Many has many tables pointing back to one user as the owner. Many to Many can't be done without an additional table, for a system like any amount of users owning any amount of certain roles. The additional table establishes the relation between the two tables by making an entry for every role a user would have, with an id pointing to the user and an id pointing to the role they should have.
* What is a ‘schema’?
  * The formatting of the database's... data! Tables are set up in SQL and cannot be changed for example, that's the schema being set out.
* What is a NoSQL database?
  * A database that doesn't use SQL! Or schema, really. It's dynamic, you set it up as you wish. There's also nearly no relations. You COULD set up relations, but rather it's almost always better to just include all the information you need wherever you need it.
* How does it work?
  * Instead of tables, we have key value pairs that look like json. These are in collections, which is more akin to just sorting.
* What is inside of a Mongo database?
  * MongoDBs have their database, then in that database it has a list of collections, and each collections have documents which hold the aforementioned key value pairs of each type of data. They can even have optionally no key value pair while other sets have it in the same document. No schema makes that possible!
* Which is more flexible - SQL or MongoDB? and why.
  * MongoDB, because the schemas aren't pre-defined. You can technically modify the schema after already setting everything up, where on SQL this would be a massive pain.
* What is the disadvantage of a NoSQL database?
  * I would consider no schema to be a disadvantage, and I also consider relationships being king in SQL dbs to be a very good thing.
