# RPC

Remote Procedure Call. A high-speed, direct system-to-system interface between two microservices. Implemented by gRPC. RPC differs from REST in four main aspects:
1. The connection remains open for the entirety of the process.
1. RPC allows unique method names, e.g. “SendConfirmationEmail” -- as opposed to the HTTP verbs (GET, POST, PUT, etc).
1. RPC allows for interface interrogation by machine instead of being limited to only a human-readable specification.
1. RPC is faster.

The main disadvantage of RPC is that it requires a special library to implement and is not a standard HTTP request.
