**Pod Network**

A pod on node 1 can talk to a pod on node 2 via the IP Address. 

However IP addresses change all the time, so better to use a Service. Pod 1 can access Pod 2 using the name of the service.

The Service cannot join the POD network because the service is not a real thing. Its not a container like the pods. Lives in memory.

Services are accessible across ALL nodes via the Kube-Proxy. Kube-Proxy is a process that runs on each node. Its job is to look for a new service and managed forwarding to IPs.