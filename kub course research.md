# research

```
orphan , zombie  ===>>> cpu کند میشه  ===>>> crash میشه
```

```
zombie :  پروسه تموم شده ولی  orphan هنوز داره کار میکنه
و هردوتاشون والد parent ندارند
```


```
nginx 
```

```
bind
```

```
youtube ===>>> techworldwithnana
```

```
alocate
```

```
SWAP ===>>> حافظه مجازی
```

```
cgroup
```

```
rootfs
```

```
bootfs
```

```
image alpine
```

```
image ubuntu
```

```
7 layer OSI
```

```
packet filtering & network tools
```

```
chain مختلف
```

```
مرتضی باشلیز ===>>> sudolearn  ===>>> iptables ===>>> youtube
```

```
linux  capabilities ===>>> DECSECOPS ===>>> پینگ بندی
```

```
seccomp filtering ===>>> system call
```

```
compare daemon to service 
```

```
= دیمن بهش بگی میاد بالا
دیمن یه پروسس بک گراند
service  توسط دیمن ارائه میشه
سرویس خودش دیمن راه میندازه
```


```
compare yml, json, yaml
```

```
compare ===>>> label ===>  yaml, انتخاب ===>>> annotation ===> json, برای همه برنامه توضیحات داره
```

```
research ===>>> condition , annotation, image kubelet, component kubernetes
```

```
compare ===>>> drain, cordon
```


---

---


```
pod موقتی ها ===>>> OSI ===>>> destination IP, dstination port , source IP , source port
اگر قرار به pod ترافیکی برسه
باید ip, port  اون pod داشته باشیم
```

```
load balance  اگر ip یه چیزی رد بشه ، بالا بیاد
```

```
kubectl ===>>> kubeconfig وصل میشه
```

```
log monitoring ===>>> log stash ===>>> std out
```

```
event ===>>> iptables, dnat, cluster
```

```
k3s ===>>> systemd ===>>> sudo systemctl status k3s.services
```

```
kubctl ===>>> به عنوان باینری  ===>>> kubctl get node
```

```
netstat -nltp
```

```
netstat -nltp | grep 6443
```

```
ls /etc ===>>> تنظیمات مربوط به کانفیگ
```

```
ls /etc/rancher/k3s/k3s.yaml
```

```
CA , rootCA , APIversion ===>>> research
```

```
systemd-cgls ===>>> اسلایس و اسکوپ ببینی
```

```
slice ===>>> برای گروه بندی لینوکس یه سری اسکوپ داره، مستقیم پردازشی انجام نمیده - خودش پروسه خاصی نداره cgroup زیرمجموعه
شبیه cgroup عمل میکنه برای تقسیم بندی منابع کاربر
slice ===>>> kubepods
max slice parent
```

```
scop ===>>> runtime ===>>>  پردازشی که مدیریت کانتینر نتیجه میرسد
```

```
limit , resource ===>>> limit ===>>> max  - resource ===>>> min
```

```
kubectl describe pod nginx --deployment
```

```
sudo vim /sys/fs/cgroup/kubepods.slice  ===>>> besteffor بیشترین مقدار ممکن از منابع
```

```
compare ===>>> drain . cordon
```

```
kubectl delete -f deploy-nginx.yaml
```

```
kubectl delete svc
```

```
guaranteed  ===>>> بالاترین اولویت  ===>>> burstable  ,  besteffor ===>>> پایین ترین اولویت
```

```
container ===>>> containerd ===>>> run اجرا میکنه
```

```
multi node ===>>> docker swarm , kubernetes
```

```
replica ===>>> orkristrator
```

```
روی node ===>>> درست نیست container ===>>> اجرا کنیم
access, memory, burstable
منابع داریم ===>>>  namespace , cgroup محدود کنیم
```

```
CRI , kubelet , process بیافته ===>>> shim
```

```
component kubernetes ===>>> 6 or 7 component
```

```
kubeletmanager ===>>> master, workload
```

```
image kubelet
```

```
conditions , annotation ===>>> research
```

```
host port:0/TCP
```

```
اطلاعات همه describe
```

```
export kubeconfig=~/config
focker.ir/nginx
```


```
kubectl logs nginx
```


```
compare ===>>> lable ===>>> yaml , annotation ===>>> json
at yaml میشود json  استفاده کرد
```


```
kubectl get pods -l app=nginx
```

```
ingress ===>>> age, service
```

```
concept ===>>> kube-proxy
```

```
spec:
  replica:2
  spec:
    containers:nginx 1,14,2
```

```
sudo crictl images
```

```
kubectl get pod -w
```

```
kubectl rollout deployment ===>>> restart
```


```

```

```

```


```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```
