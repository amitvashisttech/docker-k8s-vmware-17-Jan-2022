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
