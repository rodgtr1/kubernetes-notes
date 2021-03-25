**See All**
```
kubectl get all
```

**Get**
```
kubectl get *
            nodes
            pods
            replicaset
```

**Delete**
```
kubectl delete replicaset my-replicaset
               pod
               serviceaccounts
               --all pods
```

**Create**
Create deployment
```
kubectl create deployment --image=nginx nginx
```

Create pod from file
```
kubectl create -f replicaset-definition.yml
```

Generate Deplyment YAML File
```
kubectl create deployment --image=nginx nginx -o yaml > nginx-deployment.yaml
```

Generate Deplyment YAML File DRY RUN
```
kubectl create deployment --image=nginx nginx --dry-run=client -o yaml
```

**Run**
```
kubectl run nginx --image-nginx
```

**Replace**
```
kubectl replace -f replicaset-definition.yml
```

**CHANGING NUMBER OF REPLICAS**
```
kubectl replace -f replicaset-definition.yml
or
kubectl scale --replicas=6 replicaset myapp-replicaset
or
kubectl scale replicas=6 replicaset-definition.yml  <-- Using filename as input will update scale but not the number in the file
```