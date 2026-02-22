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
sudo strace ls → نمایش system callهای اجرای دستور ls```
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
