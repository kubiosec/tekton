### Things todo

- Create a secret for AWS accounts
- Create env entries

```
      env:
      - name: AWS_ACCESS_KEY_ID
        valueFrom:
          secretKeyRef:
            name: $(params.aws-creds)
            key: AWS_ACCESS_KEY_ID
      - name: AWS_SECRET_ACCESS_KEY
        valueFrom:
          secretKeyRef:
            name: $(params.aws-creds)
            key: AWS_SECRET_ACCESS_KEY            
```
```
kubectl create secret generic aws-creds --from-literal AWS_ACCESS_KEY_ID=xxxxxxx --from-literal AWS_SECRET_ACCESS_KEY=xxxxxxx
```
