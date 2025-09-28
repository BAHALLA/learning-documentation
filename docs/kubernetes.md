# Kubernetes

Kubernetes (often called **K8s**) is an open-source platform for **automating deployment, scaling, and management of containerized applications**.  
It provides a powerful, declarative API so you can describe the desired state of your workloads and let the system maintain it.

---

## 🌐 Overview

* **Container Orchestration** – schedules and runs containers across a cluster of machines.
* **Declarative Configuration** – you describe the desired state (e.g., “3 replicas”) and Kubernetes continuously works to match it.
* **Self-Healing** – automatically restarts or reschedules failed containers.
* **Horizontal Scaling** – add or remove pods seamlessly based on demand.

---

## 🏗️ Architecture

The diagram below shows the main components of a Kubernetes cluster:

![Kubernetes Architecture](images/kube-archi.png "Kubernetes architecture")

**Key Pieces**

* **Control Plane**
  * **API Server** – central management entrypoint.
  * **Scheduler** – decides which node runs a new pod.
  * **Controller Manager** – ensures desired state (replicas, endpoints, etc.).
  * **etcd** – distributed key-value store for cluster state.

* **Worker Nodes**
  * **Kubelet** – agent that runs on each node and communicates with the API server.
  * **Kube-Proxy** – manages networking rules and service discovery.
  * **Container Runtime** – e.g., containerd or CRI-O to run the actual containers.

---

## 🚀 Next Steps

* Try the [Kubernetes Basics Tutorial](https://kubernetes.io/docs/tutorials/kubernetes-basics/).
* Explore `kubectl` commands:
  ```bash
  kubectl get nodes
  kubectl apply -f deployment.yaml

