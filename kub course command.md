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
یک پروسه فضای ایزوله شده است
```

```
executable : قابل اجراست : پروسه یه برنامه در حال اجراست
```

```
computer: disk,memory, cpu
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
cpu ===>>> scheduling ===>>> زمانبندی
```

```
inherits: ارث بری
```

```

```

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
