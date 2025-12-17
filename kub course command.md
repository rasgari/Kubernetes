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

```
