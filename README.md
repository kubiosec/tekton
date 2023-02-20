# tekton

## Getting started example 
### Deploy the tasks
```
kubectl apply -f ./task/gh-clone-task.yaml
kubectl apply -f ./task/trivy-scan-task.yaml
kubectl apply -f ./task/gh-issue-task.yaml
```

### Deploy the pipeline
```
kubectl apply -f ./pipeline/clone-scan-issue.yaml
```

### Running the pipeline
```
kubectl create secret generic git-creds --from-literal gh-token=xxxxxxx
```
Note: update `./pipelinerun/clone-scan-issue-run.yaml` referencing a existing repo
```
kubectl apply -f ./pipelinerun/clone-scan-issue-run.yaml
```
