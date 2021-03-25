**Kube Controller Manager definitions**

kubeadm setup
```
kubectl get pods -n kube-system
```
```
cat /etc/kubernetes/manifests/kube-controller-manager.yaml
```
non kubeadm setup
```
cat /etc/systemd/system/kube-controller-manager.service
```
Also...on master node
```
ps -aux | grep kube-controller-manager
```