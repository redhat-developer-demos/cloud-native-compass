# Strict Consistency

This consistency level is the “holy grail” of distributed systems. It brings ACID properties to the distributed world. It is defined as: when a client writes a value to specific key to the system, then any other read from arbitrary node will get the most up-to-date value for the key. And at the same time the operations over the properties could be grouped into blocks where those blocks defines a single non-separable unit of work where no operation from outside of the block can enter between.

In a traditional relational database model, this is achieved by using row- and set-level locks. In a distributed environment, with multiple databases, this becomes too expensive to be practical.
