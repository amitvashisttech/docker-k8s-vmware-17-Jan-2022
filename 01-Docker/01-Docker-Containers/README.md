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
```
1170  ls
 1171  docker ps
 1172  ls
 1173  cd 01-Docker/
 1174  s
 1175  ls
 1176  cd 02-Dockerfile/
 1177  ls
 1178  cd apache/
 1179  ls
 1180  cp -rf v2 v3
 1181  ls
 1182  cd v3/
 1183  ls
 1184  vim index.html
 1185  ls
 1186  vim Dockerfile
 1187  ls
 1188  docker build -t myapache:v3 .
 1189  docker images
 1190  docker run -d --name test-apache-8 myapache:v3
 1191  docker ps
 1192  curl 172.17.0.9:80
 1193  ip addr
 1194  ls
 1195  docker ps
 1196  docker run -d --name test-apache-9 -p 8080:80  myapache:v3
 1197  docker ps
 1198  netstat -tulnp
 1199  systemctl status docker
 1200  docker run -d --name test-apache-10 -p 8080:80  myapache:v3
 1201  docker run -d --name test-apache-11 -p 8081:80  myapache:v3
 1202  docker ps
 1203  cat Dockerfile
 1204  docker run -d --name test-apache-12 -P  myapache:v3
 1205  docker ps
 1206  docker run -d --name test-apache-13 -P  myapache:v1
 1207  docker ps
 1208  cat Dockerfile
 1209  docker run -d --name test-apache-14 -P  myapache:v3
 1210  docker ps
 1211  docker run -d --name test-apache-15 -p 8083:80  myapache:v1
 1212  docker ps
 1213  ls
 1214  cd ..
 1215  ls
 1216  cd ..
 1217  ls
 1218  cd ..
 1219  ls
```


# Docker Network
```
1229  docker ps
 1230  docker network ls
 1231  docker network  inspect 4781ed84cc3f
 1232  docker ps
 1233  docker ps -q
 1234  docker kill $(docker ps -q)
 1235  docker ps
 1236  docker rm $(docker ps -qa)
 1237  docker network  inspect 4781ed84cc3f
 1238  docker ps
 1239  docker network  ls
 1240  docker network create my-net
 1241  docker network  ls
 1242  docker network  inspect my-net
 1243  ip adr
 1244  ip addr
 1245  docker network rm my-net
 1246  docker network  ls
 1247  docker network create --help
 1248  docker network create -d bridge --subnet=172.28.0.0/16 --ip-range=172.28.5.0/24 --gateway=172.28.5.254 mybr0
 1249  docker network  ls
 1250  docker network inspect mybr0
 1251  ip addr
 1252  docker run -d --name test-apache-1 -P   myapache:v3
 1253  docker ps
 1254  docker inspect test-apache-1
 1255  docker run -d --name test-apache-2 --network mybr0  -P   myapache:v3
 1256  docker run -d --name test-apache-3 --network mybr0  -P   myapache:v3
 1257  docker ps
 1258  docker inspect test-apache-3
 1259  docker ps
 1260  curl localhost:32772
 1261  docker network ls
 1262  docker run -itd --name test-none-1 --network none busybox
 1263  docker ps
 1264  docker exec -it test-none-1 -- ip addr
 1265  docker exec -it test-none-1 ip addr
 1266  docker run -itd --name test-bridge busybox
 1267  docker ps
 1268  docker exec -it test-none-1 ip addr
 1269  docker exec -it test-bridge ip addr
 1270  ip addr
 1271  docker exec -it test-none-1 ip addr
 1272  docker exec -it test-bridge ip addr
 1273  docker run -itd --name test-host-1 --network host busybox
 1274  docker ps
 1275  docker exec -it test-host-1 ip addr
 1276  docker ps
 1277  netstat
 1278  netstat -tulnp
 1279  netstat -tulnp | grep -v rpc
 1280  docker run -d --name test-host-3 --network host myapache:v3
 1281  docker ps
 1282  netstat -tulnp | grep -v rpc
```

# Docker Volumes 
```
 1287  docker ps
 1288  docker kill $(docker ps -q)
 1289  docker rm  $(docker ps -aq)
 1290  docker volume ls
 1291  docker volume rm ca1b1721d485fc460d48e907ac205e72824343c418846a2cd1201e9183df4263
 1292  docker volume ls
 1293  docker volume create myvol
 1294  docker volume ls
 1295  docker volume inspect myvol
 1296  cd "/var/lib/docker/volumes/myvol/_data"
 1297  s
 1298  ls
 1299  cd
 1300  ls
 1301  cd -
 1302  ls
 1303  cd ../../../
 1304  ls
 1305  cd ..
 1306  ls
 1307  cd
 1308  cd docker-k8s-vmware-17-Jan-2022/
 1309  ls
 1310  cd 01-Docker/
 1311  ls
 1312  docker run -it --name volume-test-1 -v myvol:/amit busybox
 1313  docker ps
 1314  docker ps -a
 1315  docker rm volume-test-1
 1316  docker ps -a
 1317  docker volume ls
 1318  docker run -it --name volume-test-2 -v myvol:/vmware busybox
 1319  docker ps
 1320  docker run -it --name volume-test-3 -v myvol:/vmware busybox
 1321  docker ps
 1322  cd /var/lib/docker
 1323  ls
 1324  cd volumes/
 1325  ls
 1326  cd myvol/_data/
 1327  ls
 1328  cat hello.txt
 1329  pwd >> hello.txt ; date >> hello.txt ; hostname -f >> hello.txt
 1330  cat hello.txt
 1331  cd -
 1332  ls
 1333  docker ps
 1334  docker attach volume-test-3
 1335  ls
 1336  cd
 1337  docker run -d --name test-apache1 -v /var/www/html/amit -P myapache:v3
 1338  docker ps
 1339  docker inspect test-apache1
 1340  docker ps
 1341  docker volume ls
 1342  cd /var/lib/docker/volumes/7b9ac738c3b9e04719b94efe13c8bd4c2826bb1107b573567deb4661fdc9dd66/_data/
 1343  ls
 1344  echo "Hello World" > hello.txt
 1345  ;s
 1346  cd ..
 1347  s
 1348  ls
 1349  cd
 1350  ls
 1351  cd docker-k8s-vmware-17-Jan-2022/
 1352  s
 1353  ls
 1354  docker run -d --name test-apache1 /root/docker-k8s-vmware-17-Jan-2022:/var/www/html/amit:ro -P myapache:v3
 1355  docker run -d --name test-apache3 -v /root/docker-k8s-vmware-17-Jan-2022:/var/www/html/amit:ro -P myapache:v3
 1356  docker ps
 1357  docker run -d --name test-apache4 -v /root/docker-k8s-vmware-17-Jan-2022:/var/www/html/amit:ro busybox
 1358  ls
 1359  docker run -it --name test-apache5 -v /root/docker-k8s-vmware-17-Jan-2022:/var/www/html/amit:ro busybox
 1360  ls
 1361  history
 1362  docker kill $(docker ps -qa)
 1363  docker rm $(docker ps -qa)
 1364  docker volume ls
 1365  docker volume ls -q
 1366  docker volume rm $(docker volume ls -q  )
 1367  docker volume ls
 1368  ls
 1369  history
 1370  ls
 1371  vim 01-Docker/01-Docker-Containers/README.md
 1372  cat 01-Docker/01-Docker-Containers/README.md

```
