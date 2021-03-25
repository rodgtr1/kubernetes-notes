**Get pods in particular namespace**
```
kubectl get pods --namespace=kube-system
```

**Get pods in all namespaces**
```
kubectl get pods --all-namespaces
```

**Create pod in particular namespace**
```
kubectl create -f pod-definition.yml --namespace=dev
```

**Create Namespace**
```
kubectl create namespace dev
```
or
```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: dev
```

**Switch namespaces**
```
kubectl config set-context $(kubectl config current-context) --namespace=dev
```