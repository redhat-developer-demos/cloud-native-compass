# Ambassador Containers

An Ambassador container is used to create a virtual link between a service consumer and a service. This differs from an API gateway in that the `--link` option is used in the `docker run` command to link the containers. This exposes a lone interface to the world.

For example, rather than have a website call a microservice directly, an ambassador container sits between the website and the microservice, and the website makes requests to the Ambassador container. In the event that the microservice must be moved, no changes need to be made to the website. This improves the portability of the service.

As an illustration, consider:

Website → Microservice
Website → Ambassador Container → Microservice

In the second case, moving the microservice does not require a restart of the website.


In this sense, an Ambassador container provides a unified view to the world for your microservice. This is a specialization of the Sidecar pattern, where in this situation, the Ambassador does not enhance the behaviour of the main container. Instead, it is used with the only purpose of hiding complexity and providing a unified interface to services outside of the pod, in this example, the website.
