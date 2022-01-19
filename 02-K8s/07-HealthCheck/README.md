```
 356  cd 02-K8s/
  357  ls
  358  kubectl  get pods
  359  cd 07-HealthCheck/
  360  ls
  361  vim 01-helloworld-deploy-hc.yaml
  362  kubectl  apply -f 01-helloworld-deploy-hc.yaml
  363  kubectl get deploy
  364  kubectl  get pods
  365  kubectl describe pod helloworld-deployment-66fd77b9f-2m5vg
  366  kubectl  get pods
  367  kubectl  get deploy
  368  kubectl edit  deploy helloworld-deployment
  369  watch -n .5 kubectl get pods
  370  kubectl  get pods
  371  kubectl describe pod helloworld-deployment-bcf84ffff-nvzxs
  372  kubectl  get pods
  373  ls
  374  kubectl  get pods
  375  vim 02-helloworld-deploy-custom-values.yaml
  376  kubectl  get pods
  377  kubectl  delete -f 01-helloworld-deploy-hc.yaml
  378  kubectl  apply -f 02-helloworld-deploy-custom-values.yaml
  379  kubectl  get pods
  380  kubectl  describe pods helloworld-2-deployment-69ddc54654-fx2cx
  381  ls
  382  kubectl  delete -f 02-helloworld-deploy-custom-values.yaml
  383  ls
  384  vim 03-pod-prob-exec.yaml
  385  kubectl  apply -f 03-pod-prob-exec.yaml
  386  kubectl  get pods
  387  kubectl describe pod liveness-exec
  388  watch -n .5 kubectl get pods
  389  kubectl describe pod liveness-exec
  390  watch -n .5 kubectl get pods
  391  kubectl exec -it  liveness-exec -- cat /tmp/healthy
  392  watch -n .5 kubectl get pods
  393  kubectl describe pod liveness-exec
  394  kubectl exec -it  liveness-exec -- cat /tmp/healthy
  395  watch -n .5 kubectl get pods
  396  kubectl exec -it  liveness-exec -- cat /tmp/healthy
  397  watch -n .5 kubectl get pods
  398  kubectl  delete -f 03-pod-prob-exec.yaml
  399  ls
  400  vim 04-helloworld-deploy-readiness-healthcheck.yaml
  401  kubectl  apply -f 04-helloworld-deploy-readiness-healthcheck.yaml
  402  watch -n .5 kubectl get pods
  403  kubectl describe pod helloworld-deployment-77b548f7d-wz846
  404  ls
  405  kubectl delete -f 04-helloworld-deploy-readiness-healthcheck.yaml
  406  ls
  407  cd ..
  408  ls
  409  cd ..
  410  ls
  411  git add . ; git commit -m "07-HealthCheck" ; git push
```
