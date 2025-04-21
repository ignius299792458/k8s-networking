# Kubernetes DNS
The DNS service in Kubernetes provides critical name resolution:

## CoreDNS: 
The default DNS server implementation.
Service Discovery: Maps service names to their cluster IPs.

##Pod DNS Resolution: 
For Pods, DNS queries follow the pattern:

<service-name>.<namespace>.svc.cluster.local
<pod-name>.<namespace>.pod.cluster.local



# CNI (Container Network Interface)
CNI is a specification and libraries for configuring network interfaces in containers:

## Popular CNI Plugins:

-  `Calico`: Uses BGP for routing, provides network policy enforcement
-  `Flannel`: Simple overlay network focused on traffic encapsulation
-  `Cilium`: eBPF-based networking with enhanced observability and security features
-  `Weave Net`: Creates a virtual network across nodes


## Key Functions:

1. IP allocation and assignment
2. Route setup for Pod communication
3. Implementation of network policies
4. Traffic encapsulation between nodes


