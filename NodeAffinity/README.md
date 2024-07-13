# Node Affinity

This is used to assign a pod to a particular node when the operator matches the label. 

Examples of condition

1. Equals
2. In
3. Not Equsls


## To add affinity to a node
```
kubectl label node node-name disktype=ssd