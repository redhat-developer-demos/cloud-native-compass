# Protobuf

Protobuf is a mechanism to serialze structured data to be communicated
between two end-points. The structured data is defined in a .proto file
per a data definition language published by Google. The protobuf
compiler is then used to generate code, in a chosen language (C#, C++,
Dart, Go, Python, Java are supported as of now), to read and
write the structured data.
A pretty simple analogy for Protobuf is XML - which is used to communicate with web services.

In cloud native app developement world, Protobufs are used in conjunction
with gRPC.
