## DynamoDB
```sh
•	Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance
 applications at any scale.
•	NoSQL stands for "Not Only SQL" and refers to non-relational databases.
•	Non-relational databases store data without using rigid table relationships (like foreign keys or joins).
Relationships are handled differently, such as embedding or referencing within the application.
•	DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching,
 and data import and export tools.
•	It requires low cost hardware.
•	We used to say to create a Dynamo DB database, but we don't actually create a Dynamo DB database rather we
 create Dynamo DB table and then we use it to store stuff.
•	Dynamo DB tables are all managed as these independent table entities that are not related to any other tables.
•	There's no real need for an extra database container.
•	The table itself is the container for all of your objects that you're going to store.
•	NoSQL databases are designed for horizontal scaling (adding more nodes to a cluster).
•	Auto-scaling is supported in services like Amazon DynamoDB and MongoDB Atlas.
•	Vertical scaling (adding CPU/RAM to one machine) is harder and costlier at large scale
•	DynamoDB is  schema free means we do not have to define the no of columns for the table, directly we can create
 the table.
•	Example of NoSQL database: MongoDB, Cassandra(facebook), DynamoDB(amazon), Postegre, Redis
•	The primary schema is made up of a partition key and an optional sort key.
•	The partition key is used to partition data across hosts for scalability and availability.
•	If there are huge records in the table (lets say 2000 records) then partition from 1-1000 records in one host and
 rest 1001-2000 records in another host
•	Optionally We could add a sort key as well if we desired.
•	Capacity mode are of 2 types  provisioned or OnDemand capacity
•	Provision means that we create all the space immediately.
•	On demand, we grow it as we need it.
•	you can choose your read and write capacity units.
•	In other words, how many times do I want to be able to read or write to this table
•	You're charged for read write operations with Dynamo DB
•	We can also set up our auto scaling other than the default setting.
```
## Real time implementation
```sh
E-Commerce Platforms
Scenario: Storing product catalogs, shopping carts, and user sessions.

Gaming Applications
Scenario: Track player progress, scores, and game states.
```
## Demo
```sh
Entry 1
Id: 1, name: amit, course: cloud
Id: 2, qualification: BE, Country: India
Id: 3, name: andy, timing: morning
Id: 4, name: lucee, age: 22
```
