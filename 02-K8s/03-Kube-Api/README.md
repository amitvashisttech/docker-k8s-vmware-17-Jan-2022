```
 88  kubectl get pods -n kube-system
   89  kubectl get pods -n kube-system -o wide
   90  ls
   91  cd /etc/kubernetes/
   92  ls
   93  cd manifests/
   94  ls
   95  vim kube-apiserver.yaml
   96  kubectl cluster-info
   97  kubectl version
   98  kubectl api-versions
   99  kubectl api-resources
  100  curl -k https://172.31.0.100:6443
  101  kubectl proxy --address='172.31.0.100' --port=8080 --accept-hosts='.' --accept-paths='.' &
  102  curl http://172.31.0.100:8080
  103  curl http://172.31.0.100:8080/api
  104  curl http://172.31.0.100:8080/apis
  118  curl http://172.31.0.100:8080/api/v1
  119  curl http://172.31.0.100:8080/api/v1/pod
  120  curl http://172.31.0.100:8080/api/v1/pods
  121  kubectl get pods
  122  kubectl get pods -o wide
  123  kubectl describe pod hello-amit-pod
  124  netstat -tulnp | grep -i 8080
  125  kill -9 4206
  126  netstat -tulnp | grep -i 8080
  127  cd
  128  ks
  129  ls
  130  cat .kube/config
  131  kubectl config view
  132  kubectl  get nodes
  133  kubectl config get-contexts
