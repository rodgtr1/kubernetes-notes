**Kube Scheduler definitions**

kubeadm setup
```
kubectl get pods -n kube-system
```
```
cat /etc/kubernetes/manifests/kube-scheduler.yaml
```
non kubeadm setup
```
cat /etc/systemd/system/kube-scheduler.service
```
Also...on master node
```
ps -aux | grep kube-scheduler
```