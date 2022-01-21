```
 1357  ls
 1358  kubectl  apply -f 06-Service-Discovery/
 1359  ls
 1360  kubectl  get pods
 1361  kubectl describe pod database
 1362  kubectl  logs database
 1363  kubectl  logs -f database
 1364  kubectl  exec -it  database -- top
 1365  kubectl  exec -it  database -- bash
 1366  kubectl get pods -n kube-system
 1367  kubectl logs -f metrics-server-5457ffb4b8-bm222 -n kube-system
 1368  kubectl top nodes
 1369  kubectl top pods
 1370  ls
 1371  mv 19-Metrics-server 12-Metrics-server
 1372  kubectl apply -f 12-Metrics-server/
 1373  ls
 1374  cd ..
 1375  ls
 1376  git add . ; git commit -m "12-Metrics-server"; git push
 1377  ls
 1378  cd 02-K8s/
 1379  ls
 1380  mkdir 13-AutoScaling
 1381  ls
 1382  cd 13-AutoScaling/
 1383  ls
 1384  vim hpa-example.yaml
 1385  ls
 1386  cd ..
 1387  ls
 1388  kubectl delete -f 06-Service-Discovery/
 1389  kubectl top pods
 1390  kubectl get pods
 1391  kubectl top pods
 1392  kubectl get pods
```
