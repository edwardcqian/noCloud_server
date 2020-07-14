# Kubernetes
Kubernetes is a container orchestration system. It is a system that manages all the logistics of running a distributed compute cluster (networking, resource management, scheduling, etc...). This allow you to deploy a full fledged production grade service using a docker image and some configurations.

## Setting up
We are going to use k3s from rancher, the official guide can be found [here](https://rancher.com/docs/rancher/v2.x/en/installation/k8s-install/create-nodes-lb/)

Rancher is a system that manages Kubernetes clusters with extra features such as centralized authentication, cluster management UI, cluster/node health check, etc ...

### Preparation
1. Prepare your machines
    - OpenSSH
    - Docker
    - CUDA driver (if has supported GPU)
2. Setup cluster external requirements
    - [mySQL](kubernetes/mySQL/)
    - [nginx](kubernetes/nginx/)
3. [Install cluster](https://rancher.com/docs/rancher/v2.x/en/installation/k8s-install/kubernetes-rke/)
4. [Install Rancher](https://rancher.com/docs/rancher/v2.x/en/installation/k8s-install/helm-rancher/)