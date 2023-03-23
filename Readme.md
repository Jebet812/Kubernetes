# Kubernetes
It is an open source container orchestration tool that helps manage containerized applications in different deployment environments like the physical machine, virtual machines, cloud and hybrid deploynment environments.

### Why container orchestation tools?

The rise of microservices lead to increase in the use of container technology. Increase in the use of containers lead to complexity in managing the containers across various environnments hence a demand for a way to manage them. This can be done using container orchestration tools. <br>

***Container orchestration tools offers:***
* *Scalability:*: Offers applications flexibility to adjust to increasing and decreasing loads. 
* *High Availability:* Applications are always available to users and there is no down time.
* *Disaster Recovery:* Incase of a disaster  the infrastructure has a mechanism to pick up the data and restore it to the latest state preventing data loss.

### Kubernetes Terminologies


#### Kubernetes Cluster
It is made up of comntrol plane and nodes.

* **Control Plane**
Used to manage the worker nodes.
* **Worker Nodes** simple server on a virtual or physical machine.

#### Kubelet
 It is the Kubernetes CLI. It communicates with the control plane either decratively or imperatively.

 #### Pod
This is the smallest unit in Kubernetes. <br>
It is an abstraction over container. <br>
The pod creates a running environment on top of a container to abstract the container technology run time so that you can replace them if need be and also you don't directly interact with the container since you only interact with the Kubernetes layer.<br>
It usually runs one application per Pod.<br>
Each pod gets its own IP address that is used for communication with another Pod.<br>
Pods are **ephemeral** meaning the can die easily and when that happens a new one will be created and assigned a new IP address on re-creation. This can be detremental since you have to adjust the IP address everytime the Pod restarts.

#### Service and Ingress
It is a permanent IP address that can be attached to a Pod. <br>
The lifecycle of a Pod and a Service are not connected hence evades the challenge of adjusting the IP address everytime a Pod restarts.<br>
**External Service** Opens communication to external sources. An example would be a service created for an application to be accesed through a browser.
**Internal Service**A type of service that you specify when creating one. 

#### Ingress
It acts as an entry point to the cluster. A request e.g from the web will go to the Ingress which forwards to the Service.


# Resources Used
1. [Kubernetes Crash Course for Absolute Beginners [NEW]](https://www.youtube.com/watch?v=s_o8dwzRlu4&t=1s) by 
TechWorld with Nana
2. [Kubernetes Tutorial for Beginners | What is Kubernetes? Architecture Simplified!](https://www.youtube.com/watch?v=KVBON1lA9N8) by 
Kunal Kushwaha
3. [Kubernetes Documentation](https://kubernetes.io/docs/home/)
4. [MichaelCade/90DaysOfDevOps](https://github.com/MichaelCade/90DaysOfDevOps/blob/main/2022.md)

