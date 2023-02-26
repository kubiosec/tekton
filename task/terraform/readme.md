### Things todo

- Create a secret for AWS accounts
- Create env entries

```
      env:
      - name: AWS_ACCESS_KEY
        valueFrom:
          secretKeyRef:
            name: $(params.aws-creds)
            key: AWS_ACCESS_KEY
      - name: AWS_SECRET_KEY
        valueFrom:
          secretKeyRef:
            name: $(params.aws-creds)
            key: AWS_SECRET_KEY            
```
```

```
