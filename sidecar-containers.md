# Sidecar Containers

Containers that exist to assist your microservices. In Kubernetes, sidecars run within the same namespace, i.e. the same pod, and have the same lifecycle as the service it supports.

Istio is an example of a sidecar container. By routing all traffic to and from a service through the istio sidecar, it is able to control ingress and egress routing, circuit breaker support, provide observability, and more.

The goal of a sidecar container is such that support for these and other features of cloud native computing are contained outside of your source code, i.e. you don’t need to import libraries and write code to support, for example, a circuit breaker.
