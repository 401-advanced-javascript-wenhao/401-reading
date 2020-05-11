# Reading 3 - Data Modeling & NoSQL Databases - 4/15/2020

## JS Data Modeling
* Consistently describe "things" both physically (properties) and hehaviorially (actions)
* Create logic, workflows, and applications that use/modify data
* JS has 5 main data types:
  * boolean: 2 states - true or false
  * number: when arithmetic operators might happen
  * String: when representing natural language
  * Array: for bundled data
  * Object: for many layers of bundled data

## Databases
Implementation: means of interacting with the persistence layer (file, SQL, NoSQL)<br/>
Normalization and Validation: sanity check data before operating it to ensure proper format<br/>

### CRUD Basic Operations
* `CREATE` - Add a record to a database
* `READ` - Retrieve a record or records from a database
* `UPDATE` - Update a record within a database
* `DELETE` - Remove a record from a database

### SQL Database
* Relational database with rows and columns and keys etc. Example: MySQL, PostgreSQL, Oracle Database, MS SQL etc.
* Highly structured and great for reporting or tabular data

### NoSQL Database
* Document storage based. Data are stored in one record. Example: MongoDB, Cassandra etc.
* Use a special language to access data
* Typically are pure json, no real structure
* Pulls information into one record tracked by an ID
* Good for 'read-heavy' usage and frequent aggregations
* NoSQL data modeling
  * start with what you need rather than available data
  * takes up more space with duplicate data but lookup speed is the advantage
  * ORM (Object Relation Mapping) such as mongoose is used for the service layer
  * need a schema for the data types (type, required, case, enum etc.)