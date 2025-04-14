# 🚀 Kubernetes Task 5: Build a Local Cluster with Minikube

---

## 🔍 What is Minikube?

**Minikube** is a tool that lets you run a single-node Kubernetes cluster locally. It's primarily used for learning, development, and testing Kubernetes applications on your personal machine.

### ✅ Why Use Minikube?

- Runs full Kubernetes locally with minimal setup
- Great for development, practice, and prototyping
- Supports multiple container runtimes (Docker, containerd, etc.)
- Works with Kubernetes tools like `kubectl`

---

## 🔧 What is kubectl?

**kubectl** is the command-line interface (CLI) for interacting with a Kubernetes cluster. It allows you to deploy applications, inspect and manage cluster resources, and view logs or configurations.

### ✅ Why Use kubectl?

- It's the official Kubernetes CLI tool
- Can control any Kubernetes cluster (local or remote)
- Allows scripting, automation, and debugging
- Essential for managing YAML configurations and cluster health

---

## 🧰 Tools Required

- **Minikube** – runs a local Kubernetes cluster
- **kubectl** – CLI tool to interact with the cluster
- **Docker** – used by Minikube as the container runtime (optional driver)

### ✅ Check Versions

```bash
minikube version
kubectl version --client
docker --version
```

---

## ✅ Step-by-Step: Kubernetes Cluster with Minikube

---

### 🔥 a. Start Minikube Cluster

```bash
minikube start --driver=docker
```

> 📸 **Screenshot to Take**: Output of `minikube start`

---

### 📦 b. Create `deployment.yaml`

Apply the deployment:

```bash
kubectl apply -f deployment.yaml
```

> 📸 **Screenshot to Take**: Output of `kubectl get deployments` and `kubectl get pods`

---

### 🌐 c. Expose App using `service.yaml`

Apply the service:

```bash
kubectl apply -f service.yaml
```

Access the app:

```bash
minikube service nginx-service
```

> 📸 **Screenshot to Take**: Output of `kubectl get svc`

---

### 🔍 d. Check Pods

```bash
kubectl get pods
```

> 📸 **Screenshot to Take**: Pods running status

---

### 📈 e. Scale the Deployment

Scale replicas from 2 to 5:

```bash
kubectl scale deployment nginx-deployment --replicas=5
```

Check new pods:

```bash
kubectl get pods
```

> 📸 **Screenshot to Take**: Output before and after scaling

---

### 🧾 f. Describe & View Logs

Describe the deployment:

```bash
kubectl describe deployment nginx-deployment
```

Get logs from a pod:

```bash
kubectl logs <pod-name>
```

> 📸 **Screenshot to Take**:
> - Output of `kubectl describe deployment nginx-deployment`
> - Output of `kubectl logs <pod-name>`


---

## 🎯 Summary

By completing this task, I have learned:

- ✅ How to start and use Minikube
- ✅ Basics of `kubectl` commands
- ✅ How to write and apply Kubernetes Deployment and Service YAMLs
- ✅ How to scale a deployment
- ✅ How to view logs and describe Kubernetes resources
