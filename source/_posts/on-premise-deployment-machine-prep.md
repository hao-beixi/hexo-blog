---
title: on-premise deployment machine prep
date: 2021-10-21 13:33:52
tags:
---
# On-Premise Deployment Machine Prep
## 1. Re-image the system
### 1.1 Prepare the bootable USB
https://ubuntu.com/download/desktop
download Ubuntu 20.04.3 LTS

note that the server version does not have GUI


use Rufus to make the drive
https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview

tap F11 to enter boot menu to boot from USB

if stuck on Read package list, it probably already finished installing

## 2. Prepare the ubuntu for install

### 2.1 install myssh
https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/

https://linuxconfig.org/how-to-find-my-ip-address-on-ubuntu-20-04-focal-fossa-linux
ip r 
### 2.2 Install docker and kubernetes

disable swap 
sudo swapoff -a  
https://phoenixnap.com/kb/install-kubernetes-on-ubuntu

if you are in China
https://www.cnblogs.com/leisurelylicht/p/Ubuntu-guo-nei-an-zhuang-kubernetes.html

https://www.jianshu.com/p/f2d4dd4d1fb1

### 2.3 Configure the k8s to make node

docker pull registry.cn-hangzhou.aliyuncs.com/google_containers/kube-apiserver:v1.22.2


# shell scripts for using aliyuncs to bypass google
```docker login --username=<your-user-name> registry.cn-beijing.aliyuncs.com
```

```
images=(
kube-apiserver:v1.22.2
kube-controller-manager:v1.22.2
kube-scheduler:v1.22.2
kube-proxy:v1.22.2
pause:3.5
etcd:3.5.0-0
coredns:v1.8.4
)
for imageName in ${images[@]} ; do
	echo $imageName
	docker pull registry.cn-hangzhou.aliyuncs.com/google_containers/$imageName
	echo "pulled"
	docker tag registry.cn-hangzhou.aliyuncs.com/google_containers/$imageName  k8s.gcr.io/$imageName
	echo "tagged"
	docker rmi registry.cn-hangzhou.aliyuncs.com/google_containers/$imageName
	echo "removed"
done
```
```
docker tag registry.cn-hangzhou.aliyuncs.com/coredns:v1.8.4 google_containers/coredns/coredns:v1.8.4
```
```
kubeadm token create --print-join-command
```

https://www.padok.fr/en/blog/kubeadm-kubernetes-cluster