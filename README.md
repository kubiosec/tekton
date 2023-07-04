# Tekton


## Getting started example 
### Install tekton
More information at [https://tekton.dev/docs/pipelines/install/](https://tekton.dev/docs/pipelines/install/)
```
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```
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
Note: update `./pipelinerun/clone-scan-issue-run.yaml` referencing an existing repo
```
kubectl apply -f ./pipelinerun/clone-scan-issue-run.yaml
```
