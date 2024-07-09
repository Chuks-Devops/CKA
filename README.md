# Kubernetes

## To print env from a pod
```
kubectl exec -it myapp-pod -- printenv
```

## Demon Set
This creates a new pod on a new node

## Why Deamonset
1. Monitoring Agent
    - kubee-proxy
2. Logging Agent
    - weave-net
    - flannel
    - calico

### To get all deamon set in all nodes
```
kubectl get ds -A
```

## Cron Job
This executes repeatedly at a certain timme of the day

*  *  *  *  *

minutes hours day-of-month month   day

0-59    0-23  1-31         1-12    0-6 (sun-sat)

To Run every 5 mins
*/5 * * * *

This can be used too clean up cluster at every time or generate reports.

## Job
This executes only once. It can be used for start up scripts or pod initialization etc

