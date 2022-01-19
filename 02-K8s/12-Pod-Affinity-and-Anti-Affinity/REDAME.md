```
 656  vim 12-Pod-Affinity-and-Anti-Affinity/helloworld.yaml
  657  kubectl  apply -f 12-Pod-Affinity-and-Anti-Affinity/helloworld.yaml
  658  kubectl get pods -o wide
  659  kubectl describe node  | grep -i taint
  660  kubectl taint nodes worker2 app-
  661  kubectl describe node  | grep -i taint
  662  kubectl get pods -o wide
  663  kubectl  delete  -f 12-Pod-Affinity-and-Anti-Affinity/helloworld.yaml
```
