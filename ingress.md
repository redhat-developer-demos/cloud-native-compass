# Ingress

Ingress is collection of rules that determines or decides where to route the incoming requests to a designated cluster service.  The main purpose of ingress is to give the access to a service via an externalized URL . IngressController is the main component that helps in resolving a request to cluster service; it can also add to itself other features like LoadBalancing, proxying to provide HA-like features.

Examples include the Kubernetes Ingress Controller and Istio.
