# Objective
### To understand different components in K8S and how it works.

## K8S Components:
* **Deployment**: Its an abstraction of pod. Kind of a Blueprint of Pod. Creates a replica of pod.
* **pod**: Creates an environment where our actual applications runs, its an abstraction of container.
* **worker node**: Actual applications runs in this node. And 3 processes must be run all time in worker nodes are 
   1. Container Runtime: Docker or containerd
   2. kubelet: allow to interact container and node
   3. kubeproxy: It forward and manage requests from other nodes to access services running on pods.
* **master node**: Father of K8S, who actual take cares of worker nodes. 4 process must be run on master node.
   1. API Server: Is a cluster Gateway and a Gatekeeper who authorize an access.
   2. Scheduler: Schedule requests on worker node as per the status of worker node.
   3. Container Manager: It detects any changes on cluster such as pods die or restart.
   4. etcd: A Cluster Brain. Stores all data of cluster in key:value pairs. **Note:Does not store any app data.**
* **Service**: Attached to pod and have static IP. Two types of Services: **External Service and Internal Service**
* **ConfigMap** : An external Configuration file will made easy for us to apply any changes on pod.
* **Secret** : Again kind of config file, but to store credential and secret data in base64 encoded format.

## Project Outline:
### Running mongoexpress as an Front-end tool and mongodb as backend. Interact with mongodb, using mongo-express UI/UX. Analyze how K8S performs in ral time when running and managing applications on node.
