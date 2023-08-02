### 2- What is Consul Service Agent? Why is it used?
Consul Service Agent is a service discovery and management tool developed by HashiCorp. The Consul Service Agent performs the following tasks:
**1) Service Discovery:** Clients of Consul can register services such as API or MySQL, and other clients can be used to discover the providers of the service provided by Consul. By using DNS or HTTP, applications can easily find the services they are connected to.
**2) Health Checking:** It is used by the operator to monitor the health of the cluster. It is also used by service discovery components to prevent traffic from being directed to unhealthy hosts.
**3) KV Store:** Applications can be used from Consul's Key/Value Store for many purposes such as dynamic configuration, feature flagging, coordination and leader election.
**4) Secure Service Communication:** TLS certificates can be created and distributed to services so that Consul services can establish Mutual TLS Connection. 'Intensions' is used to define which services are allowed to communicate. 'Service Segmentation' can be easily managed thanks to 'Intensions' that change in real time instead of Complex Network Topologies and static firewall rules.
**5) Multi Datacenter:** Consul supports Multiple Datacenters. In other words, it means that Consul users don't have to worry about creating additional layers of abstraction to grow in multiple regions.

In short, Consul Service Agent is software for discovering, monitoring and managing services in distributed systems.

-> You can proceed to the next step where we will learn how to use the Consul Service Agent.