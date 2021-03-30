Service is an object just like Pods, Replicasets, etc. 

One use case is to listen to a port on the node and forward requests from that port to a port on a pod running a web application. This is called a Node Port.

## Service Types
**NodePort**
Mentioned above.

Maps a port on the node to a port on a pod. 

- TargetPort - The port that the web server is using and the Service forwards the requst to (ex. 80).
- Port - The port on the service itself (ex. 80).
- NodePort - The port on the Node itself that we access externally. NodePorts can only be a certain range, 30000 - 32767.

The service has an IP address. That's called the ClusterIP.

Will forward to multiple pods with same labels and will forward across all nodes. Same port, different ip addresses. Random balancing.

**ClusterIP**
Service creates a virtual IP inside the cluster to enable communication between services

**LoadBalancer**
Provisions a load balancer for our application. Instead of different addresses for each pod with NodePort, this gives ONE IP address to balance to all the nodes. Load Balancer has support to integrate with major cloud provider load balancers. Only works with supportive cloud platforms. If set without supportive load balancer, it will have the same effect as NodePort.