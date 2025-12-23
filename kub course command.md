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
ipnetns,
pid ایزوله نیست 
به unshare نگفتیم pid ایزوله کنه
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


---

---

# description

```
pid (1) ===>>> init  ===>>> همه چی در لینوکس فایل است
```

```
namespace : PID,  cgroup, time, user, mount, network, UTS, IPC
```

```
فضای مختلف گنجانده می شود
```


```
ppid دارند ===>>> orphan
```

```
master blain :
tools, docker, swarm, network, linux
```

```
کانتینر چیست؟ پروسه ای است که با استفاده از namespace و cgroup محدود سازی شدند
```


```
cgroups ===>>> for resourcecontrol
```

```
CPU control ===>>> I/O control ===>>> disk

network control

memory control

```

```
cgroup in action ===>>> CPU limits(timebase) , memory safety , I/O control
```

```
CPU ===>>> 2 version ===>>> cgroups1, cgroups2
```

```

```

```
یک پروسه فضای ایزوله شده است
```

```
executable : قابل اجراست : پروسه یه برنامه در حال اجراست
```

```
computer: disk,memory, cpu
```

```
image pull
```

```
کانتینر دی روی نود node  به صورت دیمن daemon نصب میشود، ایمیج pull میکنه
```

```
snapshot ===>>> mount layered ===>>> rootfs views 
```

```
tasks ===>>> create start, stop, kill, observe
```

```
disk: برنامه در رِم لود میشه، حافظه موقت
memory: سخت افزاری
cpu: پردازش و محاسبات
```

```
unreachable ===>>> کارت شبکه درست تعریف نشده
```

```
عیب یابی = دانستن + چک لیست
```

```
kernel ===>>> user space + kernel space
```

```
kublet ===>>> restart ===>>> pod نمیشه restart
```

```
kuberneties تک node اجرا میشه
```

```
continerd-shim ===>>> bridge to runc & process handling
```

```
runc ===>>> execution flow & OCI bundle usage
```

```
config.json , rootfs
```

```
CRI 7 kubelet ===>>> interaction model & responsiblities 
```

```
container runtime ( execution ) 
```

```
logs/exec/attach
```

```
OCI spec ===>>> config.json
```


```
process, root, mounts, linux, 
```

```
daemon model & PID 1 behavior
```

```
PID 1 ===>>> child  به وجود بیاره - از بین نره  ===>>> zombie process
```


```
node os & systemd  ===>>> kubelet    گزارش داده میشه - تصمیم گیرنده ، مدیریت میکنه  ===>>> containerd کارمند - انجام دهنده کار
```


```
CRI  مختلف داریم ===>>> کانتینر اجرا میکنه - همه چیز در کوبلت ببینی
```

```
SUPERVISES ===>>> restart on failure
```

```
desired state ===>>> controller ( kubelet ) 
current state ( node & runtime ) observe
```

```
کوبرنتیز ===>>> مفهوم پاد ===>>> چند پروسه در چندتا namespace  قرار میگیره
```

```
در پاد چندتا کانتینر بسازیم ===>>> 
```

```
pod sandbox  ===>>> app1, app2 ===>>> executable
```

```
pause container & pod sandbox ===>>> restart ===>>> pid  عوض میشه
```

```
parent ===>>> containerd-shim
```

```
pod namespace ===>>> owner
```

```
pstree -p id
```

```
containerd ===>>> log  نگه میداره
containerd_shim ===>>> log  نگه نمیداره
logs  توی varkubelet 
```

```
pod sand box ایزوله شن name space
```

```
termination ===>>> sigterm ===>>> sigkill & prestop
```

```
container process ===>>> runc ===>>> containerd-shim ===>>> containerd ===>>> CRI API ===>>> kubelet
```

```
خود داکر داره از containerd داره استفاده میکنه
```

```
image روی node ===>>> download
```

```
pod ===>>> namespace share
```

```
containerd ===>>> image pull
```

```
image pull ===>>> همه روی node  ورکر داشته باشی
```

```
CRI , CTL
```

```
k3s.io
```

```
کوبرنتیز تک نود
```



```
namespace, cgroup, pod
```

```
kind, minikube ===>>> k3s ===>>> cluster
```

```
kube spray داوپس هابیز
```

```
kubernetes.io
```

```
notebookllm
```

```
news.ycombinator.com
```

```
kubectl getpod -n kube-system
```





```
پروسه ها همزمان اجرا می شوند که میشه threads
```

```
slice, scope طبقه بندی
```

```
cat /proc
```

```
type mount ===>>>
shard دیفالت
private کاملا ایزوله
slive از والد ارث میگیره
```

```
network ===>>> NAT ===>>> network addres translication ===>>> ترجمه ای پی
```

```
SNAT ===>>> source network addres translication
```


```
contrainerd ابزار  ===>>> architechture & components
```

```
کانتینر یه پروسه است که ایزوله شده
```

```
runtime ===>>> containerd ===>>> content store - metadata store - snapshotter - task service
```


```
CRI = container  runtime interface
```

```
DNAT ===>>> destination network addres translication
```

```
file system =  قوانین قرار گرفتن فایل ها در کنار هم هستند
```

```
cpu ===>>> scheduling ===>>> زمانبندی
```

```
inherits: ارث بری
```

```
current ===>>> الان استفاده میکنه
```

```
شبکه =  arrival , prerouting , routing , input / forward
```

```
netfilter ===>>> packet filter ===>>> postrouting
```


```
netfilter ===>>> iptables, IPVS , connectraction , NFtables
```

```
contianerd ===>>> pull - image - snapshot - tasks
```

```
contianerd به صورت daemon روی node نصب میشود
```

```
kubernetes universe
```

```
flow ===>>> container ===>>> یک فضای ایزوله شده که پروسه داخلش
```

```
container runtime 
```

```
systemd-cgls
```

```
pod کوچکترین
```

```
pod ===>>> multi container  ===>>> storage , network   داخل پاد شیر کنند===>>> deploy
```

```
netns
```

```
kubectl ===>>> ls /usr/local/bin 
```

```
tools ===>>> kubeseal, helm, cursor, helm, kind, kor, velero
```

```
compare yml, json, yaml
```

```
kubernetes ===>>> docs, cluster
```


```
apiversion: v1
kind: pod
metadata:
name: nginx

spec:
containers:
- name: nginx
- image: nginx:1.14.2
- ports:
  - containerport: 80
```

```
ip pod ثابت نیست
```

```
statefull  تغییر پذیر
```

```
12factor micro service
```

```
12factor.net
```

```
cloud native
```

```
state full & state less
```

```
replicaset ===>>> manifest
```

```
65000 port
```

```
source ip , destination port ===>>> range 10
```

```
kubectl get no
```

```
kubectl get po -A
```

```
pod ===>>> one ip ===>>> containerd
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
kubectl ===>>> یک باینری user/local  وجود دارد
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
annotations ===>>> توضیحات - حاشیه نویسی
```

```
kubectl delete -f
```

```
pod ===>>> replicaset تعریف نشده ===>>> self link نداره
```

```
label ===>>> برچسب workload
```

```
spec:
replicas: 3
selector:
matchlabels:
app:nginx

template:
metadata:
labels:
app:nginx
spec:
containers
- name: nginx
- image: nginx:1.14.2
ports:
- containerports: 80
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
tools ===>>> k9s
```

```
probes ( L:R:S )
```

```
self link ===>>>  قابلیت به این صورت که اگر 3تا replica داشتیم - بعد ازاینکه حذف کنی دوباره خودش ایجاد کنه
```

```
3pod ===>>> service
```

```
kubectl apply -f deploy-nginx.yaml
```

```
kubectl getpod -o wide
```

```
age , ip , node  خودش میسازه
```

```
kubectl rollout restart deployment nginx-deploy  ===>>> باعث میشه range ip در  pod ها تغییر کنه
```

```
نحوه لود بالانس قابل تنظیم نیست ===>>> با iptables خود کوبرنتیز هندل میکنه
```

```
endpoint , endpoint slice  سرویس اندپوینت میسازه
```

```
kubectl apply -f simple-svc.yaml
```

```
kubectl get pod ===>>>  اطلاعات پادها
```

```
همه چیز در لینوکس فایل است
```

```
اندپوینت ها روی هر نود node نگهداری میشوند
```

```
port :  آن چیزی که به سرویس میرسد
```

```
targer port ===>>> پورت پاد
```

```
پادها از بین میرن و به وجود میان ===>>> نیاز به kind جدید داریم
```

```
پادها با سرویس صحبت کنند ===>>>  cluster بشن
```

```
cluster ip ===>>>  قرار پادها باهم در ارتباط باشند
```

```
type spec ===>>> cluster ip, node port , loadbalancer, external name ,headless
```

```
65553 - 0 ===>>> 30000 - 32767 kubernetes
```

```
kubctl get svc  ===>>> CIDR
```

```
node port ===>>> type قرار میدی
```

```
چندتا service میتونی داشته باشی که selector یکی هست
```

```
nmaespace  نام مختلف داشته باشه
```

```
pending ===>>> در انتظار
```

```
cluster ip ===>>> coredns ثبت میشه
```

```
30000 - 32000 allocate
```

```
k3s
```

```
kubectl با چی کار میکنه ===>>> kube config
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
loadbalancer خودش cluster ip  داره ===>>> node port باز میکنه
```

```
externalname service
```

```
cast.ai
```

```
headless ===>>> no cluster IP  خودش ای پی نمیگیره
```

```
kubectl logs ===>>>  لاگ میده
```

```
kubectl describe ===>>> اطلاعات پاد میده
```

```
metallb ===>>> ip بده ===>>> loadbalance کنه  ===>>> two type ===>>> BGP layer 3 &  4
```

```
volume ===>>> دیتا در فضای persistant  بماند
```

```
اگر پاد ریستارت شد دوباره از همون مسیر بخونه ===>>> دیتا از کانتینر بیرون میاره
```

```
statefulset ===>>>  دیتابیس خوب نیست برای volume
```


```
statefulset :
pod 0 شروع میشه
به ترتیب عمل میکنه
یونیک باشه
قابلیت چسبندگی داره
```

```
daemonset ===>>> node  جداگانه ===>>> راه اندازی میشه
```

```
cronjob ===>>>  یه کاری چندبار انجام بدی و سر تایم مشخص باشه
```

```
job ===>>>  یه کاری یه بار انجام بدی میندازی تو جاب با yaml  می نویسی
```

```
2 workload , 2 kind ===>>> configmap - secret
```

```
secret = فقط موقع ریستارت شدن برنامه بهش inject میشه  ===>>> base 64
```

```
password database ===>>>  توی کد نباشه
```

```
env ===>>> environment
```

```
abstration  ===>>> انتزاعی
```

```
type namespace ===>>> dev, staging, prod 
```

```
role base access control ( RBAC )
```

```
kubectl get nodes
```

```
kubectl get ns
```

```
init container ===>>> app container
```

```
PDB ===>>> pod disruption budget
```

```
restart policy ===>>> always , never , on failure
```

```
deployment ===>>>  replicaset ===>>> pod
```

```
orphane ===>>> research
مالک پاک کن ولی بچه ها رو پاک نکن - فقط ownerrefrence رو از روشون بردار
```

```
kublet GC ===>>> روی هر نود داریم 
```

```
3 type probes ===>>> liveness , readines , startup
```

```
liveness ===>>>  کی آماده بکار است
readiness ===>>> ترافیک دریافت می کند
startup ===>>> خود خوان
```

```
emptydir  ===>>> research
```

```
limit , resources ===>>> container , deployment  وجود داشته باشه
```

```
pod های موقتی ===>>> OSI ===>>> destination IP , source IP
```

```
loadbalancer ===>>>
اگر ip یه چیزی رد شد، بالا بیاد
```

```
kubctl ===>>> cube confing وصل میشه
```

```
log monitoring ===>>> log stash ===>>> std out
```


```
event ===>>> iptables, DNAT, cluster
```

```
k3s ===>>> systemd ===>>> sudo systemctl status k3s.services
```

```
kubctl ===>>> به عنوان باینری ===>>> kubctl get node
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
research ===>>> CA , rootCA, apiversion
```


```
systemd-cgls ===>>> اسلایس و اسکوپ ببینید
```

```
slice ===>>> برای گروه بندی لینوکس یه سری اسکریپت داره، مستقیم پردازشی انجام نمیده، خودش پروسه خاصی نداره، cgroup زیر مجموعه
```

```
scop ===>>> پردازشی که مدیریت کانتینر نتیجه می رسند , runtime
```

```
slice , scop ===>>> شبیه cgroup عمل میکنه برای تقسیم بندی منابع کوبرنتیز
```

---


---

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




