# CQRS

Command and Query Responsibility Segregation (CQRS) is a data storage design where the model used to write data is different from the model used to read data.

In a traditional Create, Read, Update, Delete (CRUD) database model, all create, update and delete operations -- the commands -- are executed within the same, single data model as all read operations -- the queries. As expected, this has benefits and disadvantages associated with it.

The benefits of a traditional CRUD model include the ease with which code can be constructed, the familiarity with this traditional model, and the single location of all database operations.

The disadvantages include performance bottlenecks, the mixing of various domain logic into one database, and a data model that may not agree with the Bounded Context that utilizes it.

By segregating commands and queries, some of the benefits to be gained include: a data model that matches the Bounded Context; the ability to more easily scale database operations; easier application of security restrictions.

Generating the application code to support CQRS is not possible, given the fact that the queries do not necessarily map to the underlying data structures -- but are rather a derived structure as a result of Domain Driven Design. Also, because multiple data stores are typically used, data consistency issues present themselves: data may be updated in one location before other locations (see CAP Theorem).

When data has been updated but not fully propagated, it may result in a read operation that does not contain the latest update. This is known as a “stale read”.

A common use for CQRS is in support of Event Sourcing, where all database updates are written as a stream of events, and Materialized Views are used to read data. 
