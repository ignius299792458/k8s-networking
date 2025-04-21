# k8s-networking

- Cluster Networking
- Services
- Ingress
- Networking Policies

Kubernetes networking is a complex but critical component of the Kubernetes architecture. Let me explain its key aspects in detail.
Core Networking Concepts
Kubernetes networking follows a set of fundamental principles:

1. Every Pod gets its own IP address
2. Pods can communicate with other Pods without NAT, regardless of node
3. Agents on nodes can communicate with all Pods on that node
4. Flat network space that allows consistent networking model

## Pod Networking
Every Pod is assigned a unique IP address within the cluster. This enables a clean networking model where:

`Communication between containers in a Pod`: Containers within the same Pod share the same network namespace, allowing them to communicate via localhost.
`Pod-to-Pod communication`: Pods can communicate directly using their IPs, regardless of which nodes they're running on. This is implemented through Container Network Interface (CNI) plugins like Calico, Flannel, Weave Net, or Cilium.
`Network isolation`: Despite the flat networking model, Pods are isolated by default and only expose what's explicitly defined.
