### Tasks are based on deployment in AWS
Currently tasks focussing on AWS

### Don't forget to create AWS credentials in K8S
```
kubectl create secret generic aws-creds --from-literal AWS_ACCESS_KEY_ID=xxxxxxx --from-literal AWS_SECRET_ACCESS_KEY=xxxxxxx
```
### Next todo's
- Create destroy task task / task run 
- Analyse more 'generic' naming for creds and  --- terraform apply task for aws / azure stragery ...

