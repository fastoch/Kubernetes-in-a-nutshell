# Source

https://www.youtube.com/watch?v=3FsDvRRf4cg (28 Sept 2025)

# What is K8s?

Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of 
containerized applications across clusters of hosts.  

# How does it work?

Deployments and infrastructure in Kubernetes are defined using **YAML manifests**.  
Manifests represent various resource types, and are stored inside the cluster **Control Plane**.  

Kubernetes resources are declarative, meaning that they represent a certain desired configuration state which Kubernetes is in turn responsible for orchestrating and maintaining.  

# What is a cluster?

A Kubernetes cluster consists of one or mutliple nodes that are managed by a **single** shared **control plane**.  

# What is a Node?

Each node represents a single virtual or physical host within the cluster capable of running containerized workloads.  

Nodes come in different shapes and sizes, and with different hardware capabilities, all of which Kubernetes can use to make decisions on 
how and where to distribute the cluster's workload the most efficiently.  

You can think of nodes as dividing your cluster into fragments at a hardware level.

# What are namespaces?

Namespaces in Kubernetes allow us to split things at a logical level.  
The majority of resource types in Kubernetes can be grouped together into namespaces.  

Apart from keeping things organized, namespaces offer important security benefits. 
