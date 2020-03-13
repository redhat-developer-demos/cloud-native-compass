# Pod

In Kubernetes, a pod is a collection of one or more containers that share storage and/or networking and the specifications (e.g. environment variables) to run the containers. The containers in a pod have the same IP address and port number assigned to them; Kubernetes is responsible to handle this sharing.

Pods are useful when thought of in the context of auto-scaling, where multiple instances of a service are created or destroyed rapidly and on demand, with the same URI applying at all times.
