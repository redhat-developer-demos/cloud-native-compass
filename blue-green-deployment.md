# Blue/Green Deployment

A deployment pattern to enable zero-downtime deployments by running two application versions simultaneously. Because Kubernetes handles routing to and discovery of pods, this can be done quickly using patching.

The Blue/Green Deployment model uses two application versions that are running at the same time. Assuming the Blue version is the current version of the application, the next version, or Green version, is started side-by-side with the Blue version. After the Green version is ready -- that is, once both of the versions are running simultaneously in separate pods -- the route is switched from Blue to Green. At this moment, the newer version of the software is in being accessed by any requests to the service.

This switching method -- done by patching the software-defined route -- yields zero downtime while allowing an almost-immediate switch back to the Blue version if necessary (by patching the route again). While both versions are running, switching between them can be done rapidly by a route patch. When it has been determined which version is superior -- hopefully the Green version -- the inferior version can be terminated. 
