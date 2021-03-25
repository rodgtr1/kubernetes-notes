### Created at startup
* kube-system
* default
* kube-public

Within a namespace, resources can refer to each other simply by their service names
```
mysql.connect("db-service")
```

In another namespace, must add the namespace (ex: dev) to refer to service
```
mysql.connect("db-service.dev.svc.cluster.local")
```

When a service is created a DNS entry is automatically added in this format.

db-service = *Service Name*
dev = *Namespace*
svc = *Service*
cluster-local = *domain*

Can add namespace in pod definition file in metadata section