Doesn't actually place the pods. That's the job of the Kubelet. 

Kube scheduler decides which pod goes on which node (according to size, rules, etc

Runs as a service - kube-scheduler.service