# kuberneties course command

```
ps
```


```
top
```


```
htop
```


```
free -h
```


```
strace
```


```
sudo strace ls
```


```
kill -s9
```


```
pstree
```


```
kill -s9
```

```
cat /etc/passwd , bash, shell
```

```
ps
```

```
top
```

```
htop
```

```
free -h
```

```
htop ===>>> F5
```

```
strace ===>>> system call interface
```

```
sudo strace ls
```

```
ls /proc
```

```
/proc = لیست پروسه ها
```



```
cat /proc/self/status
```

```
/sys  ===>>> file system
```

```
cat /usr/bin/cat
```

```
pstree
```

```
unshare
```

```
pstree -p
```

```
bash, /bin/bash
```

```
sudo lsns ===>>> لیست namespace
```


```
sudo ls /proc/l/ns
```


```
sudo unshare -p -f -u -n -m --mount -proc bash
```


```
sudo unshare -p -f --mount -proc bash
```

```
sudo unshare -pid --fork /bin/bash
```

```
unshare --help
```

```
systemd
```

```
ip a
```

```
ps
```

```
ps aux
```

```
sleep 100&
```

```
hostname dibaro
```

```
hostname new
```

```
sudo lsns | grep  unshare
```

```
mount --bind /tmp/mnt
```

```
telnet google.com 80
```

```
telnet localhost 80
```

```
nsenter -target pid --net  ===>>> tshoot
```

```
docker exec -it mycluster
```

```
docker logs
```

```
docker exec
```


```
nsenter ===>>> runc, crictl ===>>> tools
```

```
ls / sys/fs/cgroup/   ===>>>file system
```

```
ls /proc ===>>> پروسه proc
```

```
systemd -cgls ===>>> لیست cgroup 
```


```
lsmem
```


```
id
```

```
htop
```

```
sudo mkdir my container  ===>>> cd /sys/fs/cgroup ===>>> این کانتینر پیش فرض cgroup میسازه
```

```
pstree -p 13404
```

```
yes > /dev/null ===>>> چاپ خالی
```

```
ls /boot
```

```
ls /proc
```


```
sudo iptables -l
```


```
sudo iptables -l -n -v  ===>>>  چه رول هایی وجود دارد
```

```
sudo nft list tables 
```

```
ipt
```

```
netfilter ===>>> firewalls
```

```
sudo ufw status
```

```
sudo iptables -F
```

```
IPVS ===>>> iptables رول های دسترسی  ===>>> حاج غلامعلی
```

```
curl -I google.com
```

```
sudo conntrack -l
```


```
ipgenetrator ===>>> SNAT, DNAT
```

```
sudo capsh
```

```
sudo setcap cap-net-rax.ep /bin/ping
```

```
sudo getcap /usr/bin/ping
```

```
containerd ===>>> containerd -shim ===>>> your -app
```

```
pstree -p id
```

```
containerd ===>>> image pull
```

```
container runtime 
```

```
systemd-cgls
```

```
netns
```

```
kubectl ===>>> ls /usr/local/bin 
```

```
kubectl get node
```

```
kubectl get pode -A
```

```
kubectl apply -f pod-sample.yml
```

```
kubectl get pod -o wide
```

```
kubectl get pod
```

```
kubectl delete pod nginx
```

```
kubeconfig
```

```
kubectl create -f pod-sample.yaml
```

```
kubectl apply -f pod-sample.yaml
```

```
kubectl get pod nginx -o yaml
```

```
kind: pod
```

```
kubectl delete -f
```


```
kind: deployment
```

```
kubectl apply -f
```

```
deploy-nginx.yaml  ===>>> name, ready, status, restart, age
```

```
kubectl apply -f deploy-nginx.yaml
```

```
kubectl getpod -o wide
```

```
kubectl rollout restart deployment nginx-deploy  ===>>> باعث میشه range ip در  pod ها تغییر کنه
```

```
kubectl apply -f simple-svc.yaml
```

```
kubectl get pod ===>>>  اطلاعات پادها
```

```
kubctl get svc  ===>>> CIDR
```

```
kubectl  get node
```

```
kubectl get pod -n kube-system
```

```
netstat -nltp ===>>> portward
```

```
ss -ntpl | grep 31440
```

```
kubctl delete -f deploy-nginx
```

```
externalname service
```

```
kubectl logs ===>>>  لاگ میده
```

```
kubectl describe ===>>> اطلاعات پاد میده
```

```
kubectl get nodes
```

```
kubectl get ns
```

```
k3s ===>>> systemd ===>>> sudo systemctl status k3s.services
```

```
netstat
```

```
nltp
```

```
nltp | grep 8443
```

```
ls /etc ===>>> تنظیمات مربوط به کانفیگ
```

```
ls /etc/rancher/k3s/k3s.yaml ===>>> vim
```

```
systemd-cgls ===>>> اسلایس و اسکوپ ببینید
```

```
kubectl describe pod nginx-deployment
```

```
sudo vim /sys/fs/cgroup/kubepods.slice
```

```
kubectl delete -f deployment-nginx.yaml
```

```
kubectl delete svc
```

```
kubectl logs nginx
```

```
kubectl get pods -l app=nginx
```

```
sudo crictl images
```


