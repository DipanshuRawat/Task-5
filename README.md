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
```

![Screenshot 2025-04-14 115634](https://github.com/user-attachments/assets/6fc319e8-de71-4ab4-bee6-87bba6f01651)

```
kubectl version --client
```
![Screenshot 2025-04-14 115648](https://github.com/user-attachments/assets/feaa1441-a244-4c4d-9c61-9acb59bc326e)

```
docker --version
```
![Screenshot 2025-04-14 115701](https://github.com/user-attachments/assets/2d7b5c6f-d184-4e77-a620-abaa9f80a0ce)

---

## ✅ Step-by-Step: Kubernetes Cluster with Minikube

---

### 🔥 a. Start Minikube Cluster

```bash
minikube start --driver=docker
```

![Screenshot 2025-04-14 120901](https://github.com/user-attachments/assets/2deac5c1-77b2-497d-823c-e2f87ab5e51b)

---

### 📦 b. Create `deployment.yaml`

Apply the deployment:

```bash
kubectl apply -f deployment.yaml
```
![Screenshot 2025-04-14 120950](https://github.com/user-attachments/assets/d589c819-26b0-4df6-9ba0-39507ca7f19a)

---

### 🌐 c. Expose App using `service.yaml`

Apply the service:

```bash
kubectl apply -f service.yaml
```
![Screenshot 2025-04-14 121024](https://github.com/user-attachments/assets/6cfc2ae7-92ea-4a15-92b3-e0f246b52ae1)

Access the app:

```bash
minikube service nginx-service
```

![Screenshot 2025-04-14 121136](https://github.com/user-attachments/assets/145fd510-93a3-4e27-a4cb-317b10631faa)

![Screenshot 2025-04-14 121121](https://github.com/user-attachments/assets/5503681b-d156-4792-b765-b6f8cb5b4116)

---

### 🔍 d. Check Pods

```bash
kubectl get pods
```

![Screenshot 2025-04-14 121204](https://github.com/user-attachments/assets/9a42f8ac-4eed-49e2-96df-be60d21aff3f)

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

![Screenshot 2025-04-14 121228](https://github.com/user-attachments/assets/080017ab-60fa-4720-a34d-56aeb07b99fb)

---

### 🧾 f. Describe & View Logs

Describe the deployment:

```bash
kubectl describe deployment nginx-deployment
```
![Screenshot 2025-04-14 121337](https://github.com/user-attachments/assets/8bb6a809-13e7-4c69-b4bb-9f806ed04dbe)

Get logs from a pod:

```bash
kubectl logs <pod-name>
```
![Screenshot 2025-04-14 121228](https://github.com/user-attachments/assets/d20d054b-340a-4cb6-a122-63807ee1a53a)

---

## 🎯 Summary

By completing this task, I have learned:

- ✅ How to start and use Minikube
- ✅ Basics of `kubectl` commands
- ✅ How to write and apply Kubernetes Deployment and Service YAMLs
- ✅ How to scale a deployment
- ✅ How to view logs and describe Kubernetes resources
