# kub course command

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
kublet ===>>> restart ===>>> pod نمیشه restart
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
فضای مختلف گنجانده می شود



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




