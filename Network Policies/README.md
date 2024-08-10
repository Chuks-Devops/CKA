# Network Policy
Network Policy is used to create a set of rules in order to restrict communication between pods. 


## Container Network Interface
This makes it possible for kubernetes nodes to communicate

## Examples of Container Network Interface
- Weave-net
- Flannel
- Calico
- Cilium
- Kindnet(For kind and minikube)

## To view network policy
```
kubectl get netpol
```
## To scale replicas 
```
scale deploy coredns replica=2 -n=kubesystem
```

## Link to install Calico
```
https://docs.tigera.io/calico/latest/getting-started/kubernetes/kind
```