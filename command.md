# command

🚀 مهم‌ترین دستورات Kubernetes (K8s Cheat Sheet)
📌 1. اطلاعات کلی کلاستر
```
kubectl version
kubectl cluster-info
kubectl get nodes
kubectl describe node <node-name>
```
📌 2. مدیریت Resourceها
🔹 لیست گرفتن:
```
kubectl get pods
kubectl get pods -A            # همه Namespace‌ها
kubectl get svc
kubectl get deployments
kubectl get ns
kubectl get events --sort-by=.metadata.creationTimestamp
```
🔹 خروجی با جزئیات:
```
kubectl get pods -o wide
kubectl get pods -o yaml
kubectl get deploy -o wide
```
📌 3. ساخت، آپدیت، حذف Resource
🔹 ساخت (apply):
```
kubectl apply -f app.yaml
```
🔹 حذف:
```
kubectl delete -f app.yaml
kubectl delete pod <pod-name>
kubectl delete deploy <deploy-name>
```
📌 4. دیباگ و عیب‌یابی
🔹 بررسی وضعیت Pod:
```
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl logs -f <pod-name>            # Live logs
kubectl logs <pod-name> -c <container-name>
```
🔹 وارد شدن به Pod:
```
kubectl exec -it <pod-name> -- bash
kubectl exec -it <pod-name> -- sh
```
🔹 ایجاد Pod برای دیباگ:
```
kubectl run tmp --rm -it --image=busybox -- sh
```
📌 5. مدیریت Deployment
🔹 اسکیل:
```
kubectl scale deploy <deploy> --replicas=3
```
🔹 ری‌استارت:
```
kubectl rollout restart deployment <deploy-name>
```
🔹 وضعیت رول‌اوت:
```
kubectl rollout status deployment <deploy-name>
kubectl rollout history deployment <deploy>
```
📌 6. مدیریت ConfigMap و Secret
🔹 ساخت:
```
kubectl create configmap myconfig --from-file=config.json
kubectl create secret generic mysecret --from-literal=pass=1234
```
🔹 مشاهده:
```
kubectl get configmaps
kubectl get secrets
```
🔹 نمایش محتوا:
```
kubectl get configmap myconfig -o yaml
kubectl get secret mysecret -o yaml
```
📌 7. Port Forward

برای تست سرویس‌ها بدون LoadBalancer:

```
kubectl port-forward svc/myservice 8080:80
kubectl port-forward pod/mypod 9090:9090
```
📌 8. Namespace مدیریت
```
kubectl get ns
kubectl create ns test
kubectl delete ns test
kubectl config set-context --current --namespace=test
```
📌 9. Context و kubeconfig
```
kubectl config get-contexts
kubectl config use-context <context-name>
kubectl config view
```
📌 10. Troubleshooting Node
```
kubectl describe node <node>
kubectl get pods -A -o wide | grep <node>
```
📌 11. Snapshot گرفتن از Resource
```
kubectl get deploy <name> -o yaml > backup.yaml
```
📌 12. پاکسازی Resourceهای مشکل‌ساز
```
kubectl delete pod <pod> --force --grace-period=0
```
