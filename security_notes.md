## Things to consider / test /research

### 1. cosnider using container images w/ ENTRYPOINT and not COMMAND
- use  `args:` and avoid `scripts`
- in case of `script`, check passed parameters (cmd injection ?  TBT)

### 2. consider not using shared https://hub.tekton.dev/
- insecure / vulnerable container images in shared tasks
- 
