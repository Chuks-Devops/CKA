# Node Affinity

This is used to assign a pod to a particular node when the operator matches the label. 

Examples of operators

1. Equals
2. In
3. Not Equsls
4. Exists


## To add affinity to a node
```
kubectl label node node-name disktype=ssd

## Properties in Node Affinity

- requiredDuringSchedulingIgnoredDuringExecution
    - It cannot schedule the pod if the requirement is not met

- preferredDuringSchedulingIgnoredDuringExecution
    - It would schedule the pod even though the requirement is not met but wouuuld prefer if the requirement is met
