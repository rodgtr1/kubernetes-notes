**Where is the server?**
```
kubectl get pods -n kube-system
```

**API Server definitions**
kubeadm setup
```
cat /etc/kubernetes/manifests/kube-apiserver.yaml
```
non kubeadm setup
```
cat /etc/systemd/system/kube-apiserver.service
```
Also...on master node
```
ps -aux | grep kube-apiserver
```