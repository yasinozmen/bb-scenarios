# HashiCorp - Consul
In the previous step, we talked about the concepts we need to know in order to better understand Consul. Now we will explain the topics such as What is Consul, What is it Used for?, What are Consul Features?, Consul's Architecture and Components.
## 1- What is Consul and what is it used for?
Consul, also known as Consul Service Discovery, is a service mesh solution developed by the HashiCorp company that provides a full-featured control panel with configuration management and network segmentation functions.
## 2- What are the Consul Properties?
**a) Service Discovery:** Clients of Consul can register services such as API or MySQL, and other clients can be used to discover the providers of the service provided by Consul. By using DNS or HTTP, applications can easily find the services they are connected to.
**b) Health Checking:** It is used by the operator to monitor the health of the cluster. It is also used by service discovery components to prevent traffic from being directed to unhealthy hosts.
**c) KV ​​Store:** Applications can be used from Consul's Key/Value Store for many purposes such as dynamic configuration, feature flagging, coordination and leader election.
**d) Secure Service Communication:** TLS certificates can be created and distributed to services so that Consul services can establish Mutual TLS Connection. 'Intensions' is used to define which services are allowed to communicate. 'Service Segmentation' can be easily managed thanks to 'Intensions' that change in real time instead of Complex Network Topologies and static firewall rules.
**e) Multi Datacenter:** Consul supports Multiple Datacenters. In other words, it means that Consul users don't have to worry about creating additional layers of abstraction to grow in multiple regions.
## 3- Consul's Architecture and Components
consul; It is a distributed system consisting of three main components: agents, servers and clients.

**Agents:** is the basic building block of Consul. Each node in the consul cluster must have a running agent. The agent is responsible for:
○ Registration services with Consul
○ Discovery services
○ Healthcheck services
○ Storing data in KV storage

**Servers:** Required for basic Consul functionality. The server is responsible for:
○ Storing and duplicating consul status
○ Choosing a leader for the cluster
○ Providing a DNS service for your applications

**Clients:** The client is used to interact with the Consul service. Clients can:
○ Explore services
○ Check the health of services
○ Store data in KV storage


-> *HashiCorp - We have completed step 1 of our Consul training. You can proceed to step 2 where we can install the consul.*