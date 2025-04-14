# 🚀 Task: Build a Kubernetes Cluster Locally with Minikube (Windows)

## 🧾 Objective
Deploy and manage applications in a local Kubernetes cluster using **Minikube**, **kubectl**, and **Docker** on a **Windows** system.

---

## 🛠 Tools Used

- [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop/)
- [kubectl (Kubernetes CLI)](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- Windows PowerShell or Command Prompt

---

## 📦 Prerequisites Installation

### 1. Install Docker Desktop

- Download: [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
- Install & launch Docker Desktop
- Ensure it’s running in the background

### 2. Install kubectl

Using Chocolatey (run in PowerShell as Administrator):

 -Download: [https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/]

Verify installation:
 ```
 kubectl version --client

 ```

### 3. Install minikube
- Download: [https://minikube.sigs.k8s.io/docs/start/]

Verify installation:
 ```
 minikube version

 ```
---

## ⚙️ Start Kubernetes Cluster with Minikube
Start your local cluster using Docker as the driver:

```
minikube start --driver=docker

```
## 🚀 Deploy and Expose the App
 # 1. Apply the Deployment
```
kubectl apply -f deployment.yaml
```

 # 2. Check Pod Status
```
kubectl get pods
```

 # 3. Apply the Service
```
kubectl apply -f service.yaml
kubectl get services
```

 # 4. Open the App in Browser
```
minikube service myapp-service --url

```
---

## 📈 Scale the Deployment
 **Increase pod replicas to 4:**
```
kubectl scale deployment myapp-deployment --replicas=4
kubectl get pods
```

## 🧪 Inspect and Debug Pods
 **Describe a Pod**
```
kubectl describe pod <pod-name>
```
 **View Logs**
```
kubectl logs <pod-name>
```
---