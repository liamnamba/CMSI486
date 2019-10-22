## Database Systems: Assignment Two

#### Problems from Elmasri Chapter 9:
3. 
![](https://github.com/liamnamba/CMSI486/blob/master/assignment2ERD.jpg){:height="50%" width="50%"}



7. It is not possible to map out a binary relationship that is M:N without requiring a new relation. We need to create a new relation to link the two, and it must contain a foreign key from each of the corresponding entities.

#### Problems from Elmasri Chapter 10:


3. It’s important to develop schema and application in parallel because it will ensure that your database will work well with your application. It ensures efficiency, correctness and that the project will be completed on time.

4. During the conceptual planning phase, we keep everything DBMS independent because we want to map out all possible schemas of the DB. There may be different schemas for different requirements, so we must take into account this. We use ER or EER models for now, then translate them into our chosen DBMS later.

6. For this problem I will analyze a database that holds information about sports players. The data needed will mainly be integers and varchars. These are to hold names and statistics about the different players. Front-End users would most likely be interacting with a website which sends queries to display different player statistics. These queries are navigational search queries as well as informational search queries. Each table would likely represent a different sport, with other tables containing specific player statistics such as team, age, etc. The database administrator would be the one inputting data. There are no necessary transactions because the database is mainly meant to simply store and display data. Only being able to navigate and insert new data is necessary for the administrator to successfully maintain the database.

#### Problems from Elmasri Chapter 15:


5. A functional dependency is a constraint between two sets of attributes. Functional dependencies are defined by the database designer; it is a property of the semantics. The functional dependency works on different attributes, within the tuples of different tables. 

9. When a relation is in 2NF we avoid partial dependencies. In other words, everything is fully functionally dependent. One attribute can uniquely identify another; that second attribute is called dependent on the first.

10. When a relation is in 3NF we avoid transitive dependencies. Transitive dependencies are situations where B is dependent on A, and C is dependent on B, thus making C dependent on A by transitive property.  

13. Multivalued dependencies are when a set of independent attributes are all dependent on one attribute. These happen because of 1NF. If more than one multivalued independent attribute is in the same schema, we must repeat every attribute for every other attribute to keep them independent.



#### Problems from Elmasri Chapter 21:


1. Concurrent execution is when multiple transactions are being executed on a database at the same time. Concurrency control is needed because we may run into problems when doing concurrent execution. An example would be two users using a database that contains tickets for a football game. If one user buys tickets: 1A,1B,1C, and another user tries to purchase ticket 1B, we would run into the lost update problem. If the transaction operations are interleaved, the first transaction would buy 1A, then the second transaction would buy 1B, leaving the first transaction trying to buy a ticket that is not there. We need concurrency control to stop issues like this.


6. Atomicity: a transaction is a single atomic unit. It should either be completed in its entirety or not at all. The transaction recovery system is responsible for this. This ensures accuracy within the DB and prevents many problems.
Durability: changes that occur within the DB must not be lost by any kind of failure. This is responsible for the recovery system of the DB, to make sure the data is intact and accurate. Isolation: transactions should appear as if they had been executed independently from other transactions. It is controlled by the concurrency control system. This prevents the temporary update problem. 
Consistency: transactions should be completed from beginning to end. It should take the database from one consistent state to another. Consistency is handled by the programmer to enforce integrity constraints. The state of the DB is defined by the schema, which is designed by the programmer. Constraints should be written so that the DB is always in a consistent state.


#### Problems from Van Bruggen Chapter 4:


1. The four main data structures are: Node: used to store entity information. Relationship: used to connect nodes to one another explicitly. They have a type, a start and a stop. They can loop as well. Properties: nodes and relationships are containers for properties. These are basically name/value pairs. Label: these are used to quickly and efficiently create subgraphs. You can assign labels to nodes and then Neo4j will automatically make simple data models.

3. False - you can very effectively use a graph database, but you should take precautions, for example, applying a fan-out pattern to your data.
