# In the following demo will be setting up 3 Node Kubernetes Cluster ( 1 Master & 2 Workers ) 

## For this demo will be required to have following tools installed. 
1.	Virtual Box
2.	Vagrant 
3.	Cmder / Git Bash 

## First clone this repository on your windows machine.

```
git clone https://github.com/amitvashisttech/docker-kubernetes-ericsson-20-Dec-2021.git
``` 

## Now provision three virtual machines with following commands:

```
cd docker-kubernetes-ericsson-20-Dec-2021/00-Vagrant-Setup/
vagrant.exe up


vagrant.exe status
Current machine states:

master                    running (virtualbox)
worker1                   running (virtualbox)
worker2                   running (virtualbox)
```


## Login to master node
```
vagrant.exe ssh master
```
