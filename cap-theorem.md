# CAP Theorem

CAP is a theorem explaining a tension between availability and consistency in distributed systems. The theorem states: in distributed computing, only two of the three characteristics can be guaranteed: Consistency, Availability, and Partition tolerance. However, because one of the fallacies of distributed computing includes network unreliability, the choice of partition tolerance is a given -- or forced -- constraint.

Partition tolerance is achieved when the system responds correctly despite failures. That is, proper routing, service discovery and orchestration assures that the system is working despite areas -- partitions -- of failure.

Consistency is achieved when each read of data reflects the most recent write. That is, the data is up-to-date across the network. The consistency level the CAP theorem talks about is the linearizability. Note the term consistency differs from the consistency of ACID transactions. The consistency in CAP refers to handling of concurrent data access, if multiple concurrent writes are available to readers in correct order on all nodes.
The concurrent data access is covered by “I” (isolation) in the ACID.

Availability is achieved when a non-failing node will eventually return a response. The CAP does not define any time boundary when the response has to be returned.

The definition of characteristics of availability and consistency are strong guarantees. If we relax one of them we can get a system which is partially consistent (see consistency models) but fully available.
