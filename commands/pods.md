**Pods**

Pull from repository
```
kubectl run nginx --image nginx
```


List pods in cluster
```
kubectl get pods
```

Describe pod
```
kubectl describe pod myapp-pod
```

Edit pod
```
kubectl edit pod redis
```
 - or use kubectl apply