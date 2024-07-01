
![K8S-Architect](https://github.com/Khaira11/Kubernetes-Architecture/assets/163966493/eeefec5a-e8df-4965-8caf-8436a7e6269f)

# Kubernetes-Architecture
**Kubernetes Master Node**
In Kubernetes (k8s), a master node is the control plane component responsible for managing the cluster. It coordinates and schedules tasks, maintains cluster state, and monitors node health. It includes components like API server, scheduler, and controller manager, ensuring overall cluster functionality and orchestration of containerized applications.
Master Node Components:

1) Kube API server handles administrative tasks on the master node. Users send REST commands in YAML/JSON to the API server, which processes and executes them. The Kube API server acts as the front end of the Kubernetes control plane.

2) etcd, a distributed key-value store, maintains the cluster state and configuration details like subnets and config maps in Kubernetes’ database. It’s where Kubernetes stores its information.


3) Kube-scheduler assigns tasks to worker nodes and manages new requests from the API Server, ensuring they are directed to healthy nodes.

4) Kube Controller Manager task is to retrieve the desired state from the API Server. If the desired state does not match the current state of the object, corrective steps are taken by the control loop to align the current state with the desired state.

There are different types of control manager in Kubernetes architecture:

    Node Manager: It oversees nodes, creating new ones in case of unavailability or destruction.
    Replication Controller: It ensures the desired container count is maintained within the replication group.
    Endpoints Controller: This controller populates the endpoints object, connecting Services & Pods.


**Kubernetes Worker Node**

Worker nodes in a cluster are machines or servers running applications, controlled by the Kubernetes master. Multiple nodes connect to the master. On each node, multiple pods and containers operate.

Components of Worker Nodes:

1) Kubelet, an agent on each node, communicates with the master. It ensures pod containers’ health, executing tasks like deploying or destroying containers, reporting back to the Master.

2) Kube-proxy enables worker node communication, managing network rules. It ensures rules are set for containers to communicate across nodes.

3) A Kubernetes pod is a set of containers on a single host, sharing storage and network. It includes specifications for 


    
