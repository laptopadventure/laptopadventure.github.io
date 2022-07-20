# Reading 2

[Back to the table of contents](../../README.md)

## NoSQL vs SQL (Reading)

- What type of database is the best fit for the complex query intensive environment?
  - Definitely SQL over NoSQL. SQL has more things like relationships, so it also has more tools to deal with those. Because of such, it has more tools in general for complex queries.
- What type of database is the best fit for hierarchical data storage?
  - NoSQL seems better in this case over SQL, because of the simplicity and similarities to JSON. Of course JSON similarities helps with huge data.
- Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
  - SQLs scale by beefing up the server it's on. They need more and more power to handle more load as their best way to scale. NoSQLs need more servers, not beefier ones. They need more servers to handle the extra traffic as their best way to scale.

## SQL Modeling Techniques

- Among data tables, what is a one-to-many relationship and how do we “relate” them?
  - One to many relationship is one where one table might point to many other tables. For example, a flight model may have a relation to as many tickets as there are passengers taking the flight.
  - We relate them by having one table have a property that is set to the id of another table, so it can be gotten via a query.
- Prior to designing your relational database, it might be useful to blank a blank of the database tables and their relationships.
  - Draw a diagram! Diagram out your db.
- Explain the difference between a primary and foreign key.
  - Primary keys are things like your id. They can be used to uniquely identify your record.
  - Foreign keys are things like a name. They can be shared between records of the same model, and possibly they could point to the primary key of a different record. Remember, the id they point to has to be uniquely owned by ONE record, but many foreign keys could have it as a value.

## SQL vs NoSQL (Video)

- How do we treat keywords and parameters differently in SQL syntax?
  - With SQL you're using keywords and parameters to build a command to CRUD things. Starting with SELECT you feed it parameters of records you want to select and then with another keyword you'd execute an action on what was found.
- Define normalization within the context of schemas and data.
  - ALL SQL records must follow a defined Schema. Whereas in NoSQL you can have one entry hold extra values, this is not possible in SQL.
- Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
  - One to one: One table's records have a column for pointing to another table.
  - One to many: One table points to another, but that table could have any number of records from that table pointing to it.
  - Many to many: If table A can be owned by any number of relations from table B, and that table B can have any number of relations to table A, then many to many is creating an in-between table C that will handle who gets what.
