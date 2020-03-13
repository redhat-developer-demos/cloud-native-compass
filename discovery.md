# Discovery

Discovery, or Service Discovery, is the method by which a service is located in order to be invoked.  Each microservice will be registered with a service registry e.g. kubernetes, consul and the consumers can discover the service by its name.  

For example: Kubernetes has a inbuilt service registry, each kubernetes application that is deployed will be registered against its internal service registry using service name, the consumers or the other apps can lookup the service by its name which in turn return the endpoint URL
