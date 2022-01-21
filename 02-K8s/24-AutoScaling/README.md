```
1394  cd 13-AutoScaling/
 1395  ls
 1396  vim hpa-example.yaml
 1397  sl
 1398  ls
 1399  kubectl apply -f hpa-example.yaml
 1400  kubectl  get pods
 1401  kubectl  get pods -o wide
 1402  kubectl get deploy,svc,pod
 1403  kubectl top pod
 1404  kubectl get hpa
 1405  kubectl top pod
```


```
# Log Gen Command:

while true; do wget -q -O- 172.31.0.101:31001; done

```
