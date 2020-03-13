# Eventual Consistency

A weaker level of consistency that states only that the update will be executed at each node eventually; there is no assurance of the order being kept. In our example of removing your boss from your network of friends and posting about your antipathy to him you are not sure what ordering will be processed in the system but you are sure they will be processed. The post may be sent to your friends before your boss is removed from your friend list. Both operations happen, eventually, but the order is not guaranteed.

In a monolithic system with a central database, database reads are kept as current as possible by using database locks and two-phase commits. While robust, this is expensive and does not scale across a network of microservices.

In a Cloud Native computing system, where data is distributed and replicated across the network, reading data from a replicated data store may result in stale data. The principle of Eventual Consistency is the fact that, eventually, the virtual view of the data will reflect reality. However, it also results in improved performance as database locks are not felt across the network and database reads are against local data stores.
