```
 1036  docker version 
 1037  systemctl status docker 
 1038  docker images 
 1039  docker ps -a 
 1040  docker run busybox echo "Hello World" 
 1041  docker run busybox echo "Hello World - Test 2" 
 1042  docker images 
 1043  docker ps 
 1044  docker ps -a 
 1045  docker run -it busybox
 1046  docker ps 
 1047  docker ps -a
 1048  docker run -it --name test-1 busybox
 1049  docker ps 
 1050  docker ps -a 
 1051  docker ps 
 1052  docker run -it --name test-1 busybox
 1053  docker run -it --name test-2 busybox
 1054  docker ps 
 1055  docker attach test-1
 1056  docker ps 
 1057  docker kill test-2
 1058  docker ps 
 1059  docker ps -a 
 1060  docker rm test-2
 1061  docker ps -a 
 1062  docker kill test-1
 1063  docker ps 
 1064  docker ps -a 
 1065  docker start test-1
 1066  docker ps 
 1067  docker attach test-1
 1068  ls
 1069  mkdir 02-Docker-Containers
 1070  cd 02-Docker-Containers/
 1071  ls
 1072  history > README.md 
```


```
1084  docker images
 1085  ls
 1086  mkdir 03-Dockerfile
 1087  cd 03-Dockerfile/
 1088  ls
 1089  mkdir apache
 1090  ls
 1091  cd apache/
 1092  ls
 1093  vim Dockerfile
 1094  ls
 1095  docker build -t myapache:v1 .
 1096  docker images
 1097  docker run -d --name test-apache-1 myapache:v1
 1098  docker ps
 1099  docker run -d --name test-apache-2 myapache:v1
 1100  docker run -d --name test-apache-3 myapache:v1
 1101  docker run -d --name test-apache-4 myapache:v1
 1102  docker ps
 1103  netstat -tulnp
 1104  docker ps
 1105  docker  network ls
 1106  docker  network inspect 4781ed84cc3f
 1107  ip addr
 1108  docker ps
 1109  docker inspect test-apache-1
 1110  curl "172.17.0.2"
 1111  curl "172.17.0.3"
 1112  curl "172.17.0.4"
 1113  curl "172.17.0.5"
 1114  curl "172.17.0.6"
 1115  curl 172.17.0.5:80
 1116  curl 172.17.0.4:80
 1117  ls
 1118  cd ..
 1119  ls
 1120  cd apache/
 1121  ls
 1122  mkdir v1
 1123  mv Dockerfile
 1124  ls
 1125  mv Dockerfile v1/
 1126  ls
 1127  cp -rf v1 v2
 1128  ls
 1129  cd v2/
 1130  s
 1131  ls
 1132  vim index.html
 1133  ls
 1134  vim Dockerfile
 1135  docker build -t myapache:v2 .
 1136  docker images
 1137  docker run -d --name test-apache-5 myapache:v2
 1138  docker ps
 1139  curl 172.17.0.5:80
 1140  curl 172.17.0.6:80
 1141  docker run -d --name test-apache-6 myapache:v2
 1142  docker run -d --name test-apache-7 myapache:v2
 1143  curl 172.17.0.6:80
 1144  curl 172.17.0.7:80
 1145  curl 172.17.0.8:80
 1146  curl 172.17.0.9:80
```
