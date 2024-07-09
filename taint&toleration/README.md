
## Taint and Tolerration
Taint is used on a node to schedulle a certain type of pod on it but toleration is used to schedule a pod.

### Effects of Taints
1. Noschedule = This is used for newer pods
2. NoExecuuute =     This used for existinggg and new pods
3. Prefer No Shcedule - It schedules but does not guarantee it.

### To add taint to a node
```
kubectl taint nodes node-name key=gpu:NoSchedule
```


### To remove taint from a node
```
kubectl taint nodes node-name key=gpu:NoSchedule-
```
### Nodeselector
This is used to schedule a pod on a particular node

### To show lables
```
kubectl get --show-labels
```

## To run dry-run client
```
kubectl run redis --image=redis --dry-run=client -o yaml
```