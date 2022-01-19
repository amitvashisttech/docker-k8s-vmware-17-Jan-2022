```
1281  cd 10-Taint-and-toleration-with-affinity/
 1282  ls
 1283  mv helloworld-affinity.yaml 01-helloworld-affinity.yaml
 1284  ls
 1285  mv helloworld-affinity-with-tolerations.yaml 02-helloworld-affinity-with-tolerations.yaml
 1286  ls
 1287  vim 01-helloworld-affinity.yaml
 1288  ls
 1289  kubectl  apply -f 01-helloworld-affinity.yaml
 1290  kubectl  get pods
 1291  kubectl  get pods -o wide
 1292  ls
 1293  kubectl  get pods
 1294  kubectl  get pods -o wide
 1295  ls
 1296  cd ..
 1297  ls
 1298  cd 10-Taint-and-toleration-with-affinity/
 1299  ls
 1300  cp -rf 01-helloworld-affinity.yaml 00-helloworld.yaml
 1301  ls
 1302  vim 00-helloworld.yaml
 1303  ls
 1304  kubectl  apply -f 00-helloworld.yaml
 1305  kubectl get pods -o wide
 1306  kubectl  delete -f ../10-Taint-and-toleration-with-affinity/
 1307  kubectl get pods -o wide
 1308  ls
 1309  kubectl taint nodes worker2 app=myapp:NoSchedule
 1310  ls
 1311  kubectl  apply -f 00-helloworld.yaml
 1312  kubectl  apply -f 01-helloworld-affinity.yaml
 1313  kubectl get pods -o wide
 1314  kubectl  delete -f 01-helloworld-affinity.yaml
 1315  ls
 1316  vim 02-helloworld-affinity-with-tolerations.yaml
 1317  ls
 1318  kubectl apply -f 02-helloworld-affinity-with-tolerations.yaml
 1319  kubectl get pods -o wide
 1320  ls
 1321  cd ..
 1322  ls
 1323  kubectl  delete -f 10-Taint-and-toleration-with-affinity/
 1324  ls
 1325  cd ..
 1326  ls
 1327  git add . ; git commit -m "10-Taint-and-toleration-with-affinity"; git push
```
