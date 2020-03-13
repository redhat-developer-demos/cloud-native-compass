# ConfigMap

A ConfigMap is used by Kubernetes to enable the decoupling of configuration artifacts from images. Leveraging a ConfigMap keeps a container portable across environments.  

The ConfigMap API object holds key-value pairs of configuration data.  A ConfigMap can store fine-grained information like individual properties or coarse-grained information like entire configuration files or JSON blobs.

A ConfigMap should not be used to store secrets such as API keys or passwords. In that case, use Kubernetes Secrets.
