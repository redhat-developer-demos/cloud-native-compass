# Outlier

Outlier is a method or process of identifying services that are not healthy like its other peer cluster members and making them Ejected (non-serviceable for a configurable amount of time) from the list of cluster members. The Key Performance Indicator (KPI) for identifying non-healthy members could be timeout, latency, successive failures, etc.,  

We can apply Outlier detection in conjunction with Circuit Breaker - typically when one server is overwhelmed with requests, and is running out of resources to serve requests which could potentially result in service rejections, based on the number consecutive service rejections we can mark the particular service member to non-health and apply ejection.
