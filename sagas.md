# Sagas

An event-driven model that is the microservices alternative implementation of a Two-Phase Commit. A saga consists of a collection of requests and compensating transactions. Requests must be able to be aborted and must be idempotent.

Sagas are comprised of a series of compensating transactions that are coordinated by events. They are the cloud native (near) equivalent of a distributed transaction.
