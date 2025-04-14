#KUBERNETES



Minikube is a lightweight tool that lets you run a single-node Kubernetes cluster on your local machine. It’s perfect for learning, development, and testing purposes.

Key Features of Minikube:
Local Kubernetes: Spins up a local Kubernetes cluster with minimal setup.

Cross-platform: Works on Linux, macOS, and Windows.

Supports Add-ons: Like metrics-server, ingress, dashboard, etc.

Multiple drivers: You can run Minikube using different virtualization backends like Docker, VirtualBox, Hyper-V, etc.

Why Use Minikube?
Quick way to experiment with Kubernetes.

Learn how Kubernetes works without using cloud infrastructure.

Test Kubernetes deployments and apps before going to production.




How It Works (Simplified):
Minikube creates a virtual machine or container.

It installs Kubernetes components (like kubelet, API server, etc.) inside it.

You interact with the cluster using kubectl, just like you would with a cloud-hosted Kubernetes cluster





### 🚀 What is `kubectl`?

`kubectl` (pronounced **"kube control"** or **"kube cuddle"**, depending on your vibe 😄) is the **command-line tool** used to **interact with a Kubernetes cluster**.

Think of it as your **remote control** for Kubernetes — it lets you deploy applications, inspect and manage cluster resources, view logs, and much more.

---

### 🛠️ What Can You Do with `kubectl`?

Here's a quick rundown of common tasks:

| Task | Command Example |
|------|------------------|
| View cluster nodes | `kubectl get nodes` |
| View all pods | `kubectl get pods` |
| Deploy an app | `kubectl apply -f my-app.yaml` |
| Check pod logs | `kubectl logs my-pod` |
| Get detailed info | `kubectl describe pod my-pod` |
| Open a shell in a pod | `kubectl exec -it my-pod -- /bin/bash` |
| Delete a resource | `kubectl delete pod my-pod` |

---

### 🧠 How Does It Work?

- `kubectl` talks to the **Kubernetes API server**.
- It uses a config file (usually at `~/.kube/config`) to know which cluster to talk to and how to authenticate.
- When you run a command, `kubectl` sends a request to the API server, which then takes action in the cluster.

---

### ⚡ Example:

```bash
kubectl create deployment nginx --image=nginx
```
This creates a deployment running the **nginx** container. Kubernetes handles the rest.

---



🐳 What is Docker?
Docker is an open-source platform that lets you:

Package your application and its dependencies into a container

Run that container anywhere — your laptop, a server, the cloud — with consistent behavior





---

### 🔧 Command Syntax:

```bash
kubectl scale deployment <deployment-name> --replicas=<number-of-pods>
```

---

### 🧪 Example:

Let’s say you have a deployment called `nginx-deployment`, and you want to scale it to 5 pods:

```bash
kubectl scale deployment nginx-deployment --replicas=5
```

This tells Kubernetes:  
> “Hey, I want **5 pods** running for this deployment.”

---

### ✅ How to Verify:

After scaling, you can check if the pods were created successfully:

```bash
kubectl get pods
```

Or see the status of the deployment:

```bash
kubectl get deployment nginx-deployment
```

---

### 🔁 Bonus: Scale Down

To scale back down to, say, 2 pods:

```bash
kubectl scale deployment nginx-deployment --replicas=2
```

---

### 🧠 Tip:

Scaling this way is **imperative**, meaning it changes things on the fly.  
For a more **declarative** approach (preferred in CI/CD), you’d update your YAML file like this:

```yaml
spec:
  replicas: 5
```

Then apply it:

```bash
kubectl apply -f deployment.yaml
```

---






![Screenshot (109)](https://github.com/user-attachments/assets/a5132c6f-3d5c-4e39-b4a3-7eb5dc1c9c1b)



![Screenshot (110)](https://github.com/user-attachments/assets/1e428339-3fe9-44d8-ad83-d3da71309f44)


![Screenshot (111)](https://github.com/user-attachments/assets/e4db739e-4933-4b6b-8e46-f2e295731eee)



![Screenshot (115)](https://github.com/user-attachments/assets/9f942d7f-e3b7-45ce-96ae-45de76ada1f9)



![Screenshot (116)](https://github.com/user-attachments/assets/b3bea12d-79d7-4ae6-a63f-c7cc4828c3c6)



![Screenshot (113)](https://github.com/user-attachments/assets/2b951b63-ebd6-4c26-b73c-eb49fecc4e86)



![Screenshot (114)](https://github.com/user-attachments/assets/aca1a0ae-69d6-4019-a9a9-906e68b7831e)




