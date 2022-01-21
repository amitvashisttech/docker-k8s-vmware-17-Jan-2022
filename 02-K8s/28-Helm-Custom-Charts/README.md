```
1160  mkdir 28-Helm-Custom-Charts
 1161  cd 28-Helm-Custom-Charts/
 1162  ls
 1163  helm create mychart
 1164  ls
 1165  cd mychart/
 1166  ls
 1167  cat Chart.yaml
 1168  ls
 1169  vim templates/deployment.yaml
 1170  ls
 1171  vim values.yaml
 1172  ls
 1173  cd ..
 1174  ls
 1175  helm install mynginx mychart --dry-run
 1176  helm install mynginx mychart
 1177  helm list
 1178  kubectl  get deploy,rs,pod,svc
 1179  ls
 1180  helm create mypythonwebapp-chart
 1181  ls
 1182  cd mypythonwebapp-chart/
 1183  ls
 1184  vim values.yaml
 1185  cat ../../06-Service/app-svc-deployment.yaml
 1186  ls
 1187  vim templates/deployment.yaml
 1188  ls
 1189  vim values.yaml
 1190  ls
 1191  cd ..
 1192  ls
 1193  helm install mywebapp mypythonwebapp-chart --dry-run
 1194  helm install mywebapp mypythonwebapp-chart
 1195  kubectl  get deploy,rs,pod,svc
 1196  curl 172.31.0.101:31421/info
 1197  helm
 1198  helm list
 1199  helm uninstall mynginx mywebapp my-nginx-release
 1200  helm list
 1201  kubectl  get pods
```
