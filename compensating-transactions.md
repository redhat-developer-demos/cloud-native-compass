# Compensating Transactions

A compensating transaction is a one or more database operations that result in the reversal of a database transaction without affecting other database operations. The compensating transactions pattern is used in the Cloud Native Computing context, where transactions can span several microservices and should not use traditional database locking. Instead, a distributed application should implement an eventual consistency data model.

During a long-running transaction, the affected data is inconsistent. It is not until the transaction is completed that the data is consistent and correct. If the transaction should fail before all of the steps are completed, it is required that there be a method by which the transaction can be completed at a later date or canceled.

A transaction rollback is not a valid solution in this instance because the eventual consistency database model does not implement database locking. One of the challenges of database transactions in the distributed application model is that, while a long-running transaction is executing, it may affect data is multiple, dissimilar databases (e.g. a SQL database, a NoSQL data store, text files, etc.). Further, the transaction may have affected the state of another service.

The compensating transaction, then, stores all the steps necessary to recreate any transaction. It can also be used to reverse an aborted transaction from any point. Finally, it must be idempotent so that multiple unsuccessful attempts to execute the compensating transaction itself -- either to completion or rollback -- will not result in corruption of data.
