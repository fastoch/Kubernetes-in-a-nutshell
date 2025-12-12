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

Apart from keeping things organized, namespaces offer important **security** benefits, as they allow for finer control over various parts of the cluster, 
and also make sure that certain resources cannot access each other across two separate namespaces.  

# What is a pod?

The smallest deployable unit in Kubernetes.  
It represents a single instance of a containerized workload.  

A pod usually consists of a single container, though multiple can be bundled together for more advanced functionality.  

Pods are generally considered ephemeral and stateless workloads, which is why they can be configured with health checks that tell Kubernetes 
how to periodically check that your pod is functioning correctly, allowing any faulty ones to be automatically replaced.  

# What is a deployment?

Deployments are used to define a set of desired pods by configuring: 
- a pod template,
- the desired amount of pod replicas
- and various other options to configure pod behavior

Deployments and pods are just one of many examples of parent-child relationships between resources in Kubernetes.  
With the deployment being constantly responsible for ensuring that the desired number of pods is up and running.  

# What are Secrets and ConfigMaps?

ConfigMaps and Secrets can be used to store arbitrary key-value data in the cluster, which can then be consumed by pods at runtime.  

As the name suggests, ConfigMaps are intended for non-sensitive values such as runtime configuration.  
Whereas Secrets store sensitive values such as API keys or tokens.  

Both ConfigMaps and Secrets can be mounted into pods as either environment variables or entries in the file system.  

# What are services?

Services are a networking abstraction used to group a set of workloads behind a single stable network endpoint.  
A service will automatically distribute traffic to all the pods within its scope, taking into account 
