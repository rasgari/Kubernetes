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



---

```
ps → نمایش پروسه‌های فعال در شِل فعلی
```

```
top → مانیتور زنده مصرف CPU و RAM توسط پروسه‌ها
```

```
htop → نسخه گرافیکی‌تر و تعاملی‌تر top
```

```
free -h → نمایش وضعیت حافظه RAM به‌صورت خوانا
```

```
strace → رهگیری system callهای یک برنامه
```

```
sudo strace ls → نمایش system callهای اجرای دستور ls
```

```
kill -s9 → کشتن فوری یک پروسه با SIGKILL
```

```
pstree → نمایش ساختار درختی پروسه‌ها
```

```
cat /etc/passwd → لیست کاربران سیستم
```

```
bash / shell → شِل خط فرمان لینوکس
```

```
htop (F5) → نمایش پروسه‌ها به‌صورت tree
```

```
ls /proc → نمایش اطلاعات پروسه‌ها (هر PID یک پوشه)
```

```
/proc → فایل‌سیستم مجازی اطلاعات کرنل و پروسه‌ها
```

```
cat /proc/self/status → وضعیت پروسه فعلی
```

```
/sys → فایل‌سیستم تنظیمات کرنل و cgroup
```

```
cat /usr/bin/cat → نمایش فایل باینری دستور cat (غیرقابل خواندن)
```

```
unshare → ایجاد namespace ایزوله جدید
```

```
pstree -p → نمایش PID کنار نام پروسه‌ها
```

```
/bin/bash → مسیر باینری شِل bash
```

```
sudo lsns → لیست namespaceهای فعال سیستم
```

```
sudo ls /proc/*/ns → مشاهده namespaceهای پروسه‌ها
```

```
sudo unshare -p -f -u -n -m --mount-proc bash → ایجاد محیط شبه‌کانتینر
```

```
sudo unshare -pid --fork /bin/bash → اجرای bash در PID namespace جدید
```

```
unshare --help → راهنمای unshare
```

```
systemd → init system و مدیر سرویس‌ها
```

```
ip a → نمایش اینترفیس‌ها و IPها
```

```
ps aux → لیست کامل همه پروسه‌ها
```

```
sleep 100 & → اجرای بک‌گراند یک پروسه
```

```
hostname dibaro → تغییر نام سیستم
```

```
sudo lsns | grep unshare → مشاهده namespaceهای ایجادشده
```

```
mount --bind /tmp/mnt → bind mount یک مسیر
```

```
telnet google.com 80 → تست اتصال TCP به پورت 80
```

```
telnet localhost 80 → تست سرویس لوکال
```

```
nsenter -t PID --net → ورود به net namespace یک پروسه
```

```
docker exec -it mycluster → ورود به کانتینر در حال اجرا
```

```
docker logs → مشاهده لاگ کانتینر
```

```
nsenter / runc / crictl → ابزارهای سطح پایین کانتینر
```

```
ls /sys/fs/cgroup → نمایش cgroupها
```

```
systemd-cgls → نمایش tree cgroupها
```

```
lsmem → اطلاعات حافظه سیستم
```

```
id → نمایش UID و GID کاربر
```

```
mkdir /sys/fs/cgroup/... → ساخت cgroup جدید
```

```
yes > /dev/null → مصرف 100٪ CPU برای تست
```

```
ls /boot → فایل‌های بوت سیستم
```

```
sudo iptables -L → لیست قوانین فایروال
```

```
sudo iptables -L -n -v → نمایش جزئیات رول‌ها
```

```
sudo nft list tables → نمایش جداول nftables
```

```
netfilter → فریم‌ورک فایروال لینوکس
```

```
sudo ufw status → وضعیت فایروال UFW
```

```
sudo iptables -F → حذف تمام قوانین iptables
```

```
IPVS → load balancing در Kubernetes
```

```
curl -I google.com → بررسی هدر HTTP
```

```
sudo conntrack -L → نمایش connection tracking
```

```
SNAT / DNAT → ترجمه آدرس شبکه
```

```
sudo capsh → نمایش capabilityهای لینوکس
```

```
setcap cap_net_raw+ep /bin/ping → اجرای ping بدون sudo
```

```
getcap /usr/bin/ping → مشاهده capability
```

```
containerd / shim → runtime کانتینر Kubernetes
```

```
kubectl get node → نمایش نودهای کلاستر
```

```
kubectl get pod -A → نمایش همه پادها
```

```
kubectl apply -f pod.yaml → ایجاد/آپدیت resource
```

```
kubectl get pod -o wide → نمایش IP و Node پاد
```

```
kubectl delete pod nginx → حذف پاد
```

```
kubeconfig → فایل اتصال kubectl به کلاستر
```

```
kubectl get pod nginx -o yaml → مشاهده YAML کامل پاد
```

```
kind: Pod / Deployment → نوع resource در Kubernetes
```

```
kubectl rollout restart deployment → ریستارت پادهای deployment
```

```
kubectl get svc → نمایش سرویس‌ها
```

```
netstat / ss → بررسی پورت‌های باز
```

```
ExternalName service → اتصال سرویس به DNS خارجی
```

```
kubectl logs → مشاهده لاگ پاد
```

```
kubectl describe → جزئیات کامل resource
```

```
kubectl get ns → نمایش namespaceها
```

```
k3s systemctl status → وضعیت Kubernetes سبک
```

```
ls /etc → فایل‌های کانفیگ سیستم
```

```
/etc/rancher/k3s/k3s.yaml → kubeconfig کلاستر k3s
```

```
kubectl get pods -l app=nginx → فیلتر پادها با label
```

```
crictl images → لیست ایمیج‌های runtime
```
