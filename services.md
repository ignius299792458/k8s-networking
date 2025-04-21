# Services
Services solve the problem of Pod ephemerality and provide stable networking endpoints:

## Service Types

1. `ClusterIP`: Default service type that exposes the service on an internal IP accessible only within the cluster.
2. `NodePort`: Exposes the service on each node's IP at a static port. Creates a ClusterIP service automatically.
3. `LoadBalancer`: Exposes the service externally using a cloud provider's load balancer. Creates NodePort and ClusterIP services automatically.
4. `ExternalName`: Maps the service to a DNS name rather than a typical selector.
5. `Headless Services`: Used when you don't need load balancing or a single service IP (set clusterIP: None).

## `Service Discovery`
Kubernetes offers two primary methods for service discovery:

`Environment Variables`: When a Pod is run, the kubelet adds environment variables for each active service.
`DNS`: Kubernetes DNS server watches for new services and creates DNS records for each. Pods configured to use the cluster DNS server can access services by name.
