# Consistency Models

Consistency Model is used to define and describe how data acts in a distributed system, i.e. a contract between a distributed data store and the processes. It defines how the client’s reads and writes depends on each other, if the data written by of one clients can be seen by reads of the other clients.

Consistency models are listed in order of strength, from strongest to weakest. The strongest model yields the most consistent data. Better consistency normally means lower concurrency.

Strict Consistency
Linearizability
Causal consistency
Eventual consistency
