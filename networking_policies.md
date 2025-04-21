# Network Policies
Network Policies are Kubernetes resources that control traffic flow between Pods:

- `Default Behavior`: In the absence of policies, all traffic is allowed.
- `Policy Enforcement`: Network Policies are implemented by CNI plugins that support them (e.g., Calico, Cilium, Antrea).
- `Selectors`: Policies use pod and namespace selectors to identify targets.
- `Rules`: Can specify both ingress (incoming) and egress (outgoing) rules.
