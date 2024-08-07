## Commands used in the video

To generate a key file
```
openssl genrsa -out adam.key 2048
```

To generate a csr file
```
penssl req -new -key adam.key -out adam.csr -subj "/CN=adam"
```

To convert adam.csr to base64
```
cat adam.csr | base64 | tr -d "\n"
```

To view the certificate 
```
kubectl get csr myuser -o yaml > issuecrt.yaml
```

To approve a csr
```
kubectl certificate approve <certificate-signing-request-name>
```

To deny a csr

```
kubectl certificate deny <certificate-signing-request-name>
```

To decode certificate to normal text
```
kubectl <certificate-signing-request-name> | base64 -d
```


