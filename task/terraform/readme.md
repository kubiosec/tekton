### Don't forget to create AWS credentials in K8S
```
kubectl create secret generic aws-creds --from-literal AWS_ACCESS_KEY_ID=xxxxxxx --from-literal AWS_SECRET_ACCESS_KEY=xxxxxxx
```

