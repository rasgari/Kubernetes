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
apiversion: kind  ===>>> deployment ===>>> apps
expose ===>>> port هاست ===>>> port کانتینر
```

```
namespace kuber ===>>> system
```


```
kubectl run --rm -it tester --image=archlinux --namespace=mynsbash
```

```
garbage culctor ===>>> final culctor
```

```
nodeport= 30,000 & 32,000 ===>>> datacenter config
```

```
cordines ===>>> تغییر بدی ===>>> pod بالا بیاری
```

```
هر چیزی در کوبرنتیز ===>>> configurable
```

```
kube-proxy ===>>> the magic behind kubernetes services
```

```
export kubeconfig=~/config
```

```
kubectl get nodes
```

```
kubectl describe ===>>> trouble shooting
```

```
kubectl get all -n default ===>>> تمام کوبر میاره
```

```
name 4 ===>>> pod/service/deployment.apps/replicaset.apps
```

```
kubectl get pod -A ===>>> تمام pod ها
```

```
kubectl describe -n kube-system pod metrics --
```

```
kubectl logs -n kube-system me....
```


```
kubectl apply -f deploy-nginx.yaml ===>>> create
```

```
kubectl delete -f deploy-nginx.yaml ===>>> delete
```

```
netstat -nltup | grep 304
```

```
cni, kubelet ===>>> research
```

```
kubectl get pod
```

```
kubectl get svc -o wide ===>>> sourceip, destination ip
```

```
svc ===>>> فضای abreaction, abstration
```

```
docker ===>>> single node , kubernetes ===>>> multi node or worker
```

```
node worker ===>> kubelet, kubeproxy  , node master
```

```
pod up , service up
```

```
kubectl rollout restart
```

```
kubectl exec -it ping
```

```
service controller
```

```
API server
```

```
the tools for the jobs: netfilter & iptables
```

```
kube-services باید bind بشه hook forward
```

```
through kubernetes chains
```

```
sudo iptables -L ===>>> list all
```

```
kube-services all --anywhere
```

```
chain kube-services
```

```
DNAT ===>>> rewrite destination to pod,IP & target port
```

```
Hairpin NAT ===>>> plugin ===>>> research
```

```
conntrack ===>>> connection tracking
```

```
masquerd ===>>> research
```

```
kubectl describe SVC nginx-lb
```

```
sudo iptables -t nat -L kube-services -n -v
```

```
kubectl get svc -o wide
```

```
portainer.io
```

```
3 type plain ===>>> dataplain, control plain , worker plain ===>>> pod
```

```
worker ===>>> proxy, kubelet
```

```
kubectl get pod ===>>> list pod
```

```
database ===>>> etcd ===>>> حافظه کوبرنتیز brain kubernetes
```

```
etcd به عنوان pod بالا نیارید
```

```
etcd ===>> external , kuber ==>>>json
```

```
cluster  همیشه فرد باشه 3 & 5 & 7
quorum ===>>> (n/2) +1
```

```
staying login ===>>> snapshot and compaction
```

```
mtls ===>>> research  ===>>> همه چیز با mtls رمز گذاری میشود
```

```
3type CA ===>>> root CA , intermediate CA , leaf CA
```

```
tools ===>>> k9s
```

```
etcd ===>>> backup بگیری
alert داشته باشه
```

```
etcdctl ===>>> version 3
```

```
kubectl get node
```

```
worker ===>>> هیچ role نداره
```

```
kubectl drain --ignore-daemonsets --delete
```

```
sudo -i
```

```
install kubernetes ===>>> etcd, kubelet ===>>> systemd به صورت
```

```
تنظیمات لینوکس ===>>> ls /etc/
===>>> cron.d
rc0,1,2 ===>>> init 
rc0.d
rc1.d
rc2.d 
```

```
تنظیمات کوبرنتیز ===>>>
ls /etc/kubernetes
color blue ===>>> pki, ssl, manifest
```

```
ls /etc/kubernetes/ssl & /pki  ===>>> incription
```

```
cd /etc/ssl/etcd
```

```
apiserver 
```

```
tools etcdctl ===>>> install
```

```
etcdctl status ===>>> status cluster
```

```
quorum زیاد میشه
حداکثر 7 نود ===>>> 3 یا 5  نود
فرآیند تصمیم گیری طولانی میشه، کند میشه، performance  پایین میاد، latency بالا میره
5 تا نود ===>>> 2تا از دست بدید
7 تا نود ===>>> 3تا از دست بدید
```

```
folder ssl ===>>> ca, key, pem
```

```
etcdctl endpoint status --write-out==table  --endpoints=hhtps://127.0.0.1:2777
```

```
etcdctl endpoint status --cluster --write-out=table
```

```
hostname -i
```

```
etcdctl member list --write-out=table
```

```
deployment, nginx, backup===>>> snapshot
```

```
etcdctl endpoint status --cluster
start to https
connection to TLS
```

```
dfrage , dfragement ===>>> research
```

```
timeline ===>>> backup ===>>> apiserver , cluster ===>>> down 
```

```
kubespray , from scratch
```

```
mijer ===>>> zero down time
```

```
master node ===>>>  تک به تک update میشه
```

```
sigs kuber ===>>> research
```

```
sigs kuberspray ===>>> research
```

```
systemd install
```

```
the API server: the cluster hub
```

```
kube-apiserver ===>>> kubectl, kubelet, controller manager, scheduller, static pod
```

```
restful API ===>>> crud ===>>> create, read, update, delete, patch
```

```
get ===>>> read,
post ===>>> create,
patch ===>>> patch,
put ===>>> update,
delete ===>>> delete
```

```
apiversion : apps/v1
kind: deployment
spec:
replicas:3

kubernetes ===>>> api/v1 ===>>> pod,service,nodes
```

```
new kube ===>>> apis ===>>> apps /v1 , deployment
                     ===>>> batch/v1 , jobs
                     ===>>> networking.k8s.io/v1 , ingresses
```

```
apis/group/version
```

```
versioning strategy & stability
```

```
v1alpha1,v1beta1,v1
```

```
GVK ===>>> group version kind
GVR ===>>> group version resource
apis/apps/v1/namespaces/{{ns}/deployment
one kubelet run
```

```
etcd.yaml, kube.apiserver.yaml ===>>> kubelet
```

```
ls /etc/kubernetes/manifests/static
component master manifests
kube-apiserver, kube-controller-manager/  , kube-scheduler.yaml
```

```

```

```

```

```

```




