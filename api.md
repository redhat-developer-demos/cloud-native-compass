# API

Application Programming Interface. This is the "contract" that specifies what a service expects to receive and what it promises to return. This contract, or agreement, dictates the protocols, data, and methods to be used by any client. APIs can use different data formats and protocols; In the domain of Cloud Native computing, the most common pattern is the REST API Pattern.

Most RESTful services communicate via TCP, using HTTP verbs to invoke methods and JSON documents to send and receive data. Support for XML is also another viable message format, though is much less commonly used for new interfaces. XML is not recommended for new projects as it adds unnecessary complexity and introduces a larger payload between services, i.e. it takes more text to describe an XML document versus a JSON document.

For services that are exposed outside of a network, i.e. over the internet or a WAN, REST and TCP is the de facto standard for communication.

For services that communicate within a network, i.e. behind the firewall, RPC is another means for API communications. RPC, specifically implemented using gRPC (which uses protobuffers under the hood), has the advantage over REST in that it is faster and more robust than REST over TCP. 

The speed advantage is due to reduced latency and the fact that serialization and deserialization needs are reduced, saving CPU cycles.

Robustness is improved because gRPC allows a connection to be maintained between two machines while executing remote functions; gRPC also uses strongly-typed data formats with forward- and backward-compatible schema evolution.
