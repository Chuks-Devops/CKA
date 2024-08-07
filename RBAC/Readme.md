# Authorization and Authentication

To see kubernetes manifest files
```
docker exec -it nodename bash

cd /etc/kubenetes/manifests
```
To see kubernetes manifest files
```
docker exec -it nodename bash

cd /etc/kubenetes/pki
```

To see the user you are

```
kubectl auth whoami
```

To know if you can get pod
```
kubectl auth can-i get pod
```

To impersonate another user
```
kubectl auth can-i get pod --as myuser
```

To create a role
```
kubectl apply -f role.yaml
```
To create a role-binding
```
kubectl apply -f binding.yaml
```

To see roles in all namespaces
```
kubectl get roles -A
```

To login as adam
```
kubectl config set-credentials adam \
--client-key=adam.key \
--client-certificate=adam.crt
```

To set context for adam
```
kubectl config set-context adam --cluster=minikube --user=adam
```

To switch context
```
 kubectl config use-context adam
 ```

To check expiring date of crt
```
openssl x509 -noout -dates -in ../tls/adam.crt
```

To change the expiring date
```
openssl x509 -req -dates -in ../tls/adam.csr \
-CA ca.crt \
-CAkey ca.key \
-CAcreateserial -out adam.crt -days 100
```
To get ca.crt and ca.key
```
docker exec -it nodename bash
cd /etc/kubenetes/pki

```
To view config
```
kubectl config view
```


Kubernetes documentation > How to issue a certificate for a user

```
https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/
```

To get resources at the cluster level
```
kubectl api-resources -namespaced=false
```

Commands to create cluster role and cluster role binding
```
kubectl create clusterrole node-reader --verb=get,list,watch --resource=nodes


kubectl create clusterrolebinding node-reader-binding --clusterrole=node-reader --user=adam
```

Get the cluster role
```
kubectl get clusterrole | grep node-reader 
```

describe the cluster role
```
kubectl describe clusterrole node-reader 
```

