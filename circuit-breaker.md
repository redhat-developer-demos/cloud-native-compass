# Circuit Breaker

An architectural pattern to prevent an error at a single service from cascading across the system. It does this by watching service health and "tripping" the circuit after a specified number of failures.
A circuit breaker, whether implemented in code (e.g. Hystrix) or supplied by a sidecar container such as istio, has the purpose of removing a broken service from inventory until it is repaired or replaced. Working in cooperation with service routing, an open circuit can be avoided, with requests directed to correctly-functioning services instead.

A circuit can be triggered to open by server errors (500 errors) and timeout errors.

Once the circuit is closed, requests are once again routed to the service.

Within the circuit breaker the parameters to trip the breaker (to open the route to the service and suspends its availability) are set programmatically. Settings such as how many consecutive errors, or a percentage of errors over a timespan, or a limit until a timeout is triggered, are all examples of circuit breaker pattern parameters.
While the circuit breaker can be useful, full implementation of a successful circuit breaker pattern requires that the client responds to an open circuit in a graceful way, as well as log the event.
