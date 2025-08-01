<!-- 🧵 Banner -->
<p align="center">
  <img src="https://raw.githubusercontent.com/Jotheesh2002/assets/main/professional-devops-banner.gif" width="100%" alt="Professional DevOps GIF Banner"/>
</p>

<h1 align="center">🚀 TVM Infotech Assessment Task for AWS DevOps Enginner Role</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Kubernetes-v1.33-blue?style=for-the-badge&logo=kubernetes" />
  <img src="https://img.shields.io/badge/Minikube-Running-brightgreen?style=for-the-badge&logo=linux" />
  <img src="https://img.shields.io/badge/MacBook-Air%20M2-lightgrey?style=for-the-badge&logo=apple" />
</p>

<p align="center">
  <strong>✨  Kubernetes ConfigMap Demo ✨</strong><br>
  <i>🎯 Task Given by: <strong>Yogi Ma'am (Technical HR)</strong><br>🎓 Prepared by: <strong>Jotheeshwaran V</strong></i>
</p>

---

## 🧠 Project Overview

This project demonstrates the use of **Kubernetes ConfigMaps** to manage and inject configuration into pods using **two different methods**:

- 🔧 As **environment variables**
- 📂 As **volume-mounted configuration files**

It showcases how to **decouple application configs** from container images, allowing for greater **flexibility**, **portability**, and **automation** in real-world DevOps workflows.

> 📌 Designed as part of an evaluation task for **TVM Infotech Pvt. Ltd.**, under the supervision of **Yogi Ma’am (HR)**.

---

## 👨‍💻 Author

<div align="center" style="margin-top: 2rem; margin-bottom: 2rem; animation: fadeInUp 2s ease-in-out;">
  <img src="./Screenshots/joshpics.jpg" width="120" style="border-radius: 50%; border: 4px solid #2563eb; animation: pulse 3s infinite;" alt="Jotheeshwaran Avatar">
  <h3 style="color:#1d4ed8; font-weight:700; font-size:1.75rem; margin-top: 0.5rem; animation: zoomIn 1s ease-in-out;">Jotheeshwaran V</h3>
  <p style="color:#6b7280; font-size:1.05rem;">
    📧 <strong>Email:</strong> <a href="mailto:jotheeshwaranv2002@gmail.com">jotheeshwaranv2002@gmail.com</a><br/>
    🌐 <strong>Portfolio:</strong> <a href="https://unique-crepe-5ea0e0.netlify.app" target="_blank">unique-crepe-5ea0e0.netlify.app</a><br/>
    🔗 <strong>LinkedIn:</strong> <a href="https://linkedin.com/in/jotheeshwaran-v" target="_blank">linkedin.com/in/jotheeshwaran-v</a>
  </p>
</div>

---


## 📁 Project Structure

```
k8s-configmap-demo/
├── app-config.properties # Config values
├── pod-env.yaml # ConfigMap as env
├── pod-volume.yaml # ConfigMap as volume
├── screenshots/ # Task proof images
└── README.md # This file
```

---

## 🛠️ Setup Instructions

### ✅ Step 1: Start Minikube

```bash
minikube start
kubectl config use-context minikube
```
### ✅ Step 2: Create ConfigMap
```bash
kubectl create configmap app-config --from-env-file=app-config.properties
```
### ✅ Step 3: Deploy Pod Using Env Variables
```bash
kubectl apply -f pod-env.yaml
kubectl logs app-pod-env
```
### ✅ Step 4: Deploy Pod Using Volume Mount

```
kubectl apply -f pod-volume.yaml
kubectl exec -it app-pod-vol -- sh
cat /etc/config/APP_MODE
cat /etc/config/APP_PORT
```
<h2>📷 Output Screenshots</h2>

<!-- Row 1 -->
<div style="display: flex; justify-content: center; gap: 20rem; flex-wrap: wrap; margin-bottom: 20rem;">
  <div style="flex: 1 1 45%; text-align: center;">
    <h3>✅ Docker Desktop - Kubernetes Start </h3>
    <img src="Screenshots/Docker Desktop.png" alt="API Output" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px;" />
  </div>
  <div style="flex: 1 1 45%; text-align: center;">
  <h3>✅ k8 Pods Status  </h3>
    <img src="Screenshots/Pods Status.png" alt="API Output" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px;" />
  </div>
  <div style="flex: 1 1 45%; text-align: center;">
    <h3>✅ Check Logs from ENV-Based Pod </h3>
    <img src="Screenshots/Check Logs from ENV-Based Pod.png" alt="Docker Runtime" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px;" />
  </div>
  <div style="flex: 1 1 45%; text-align: center;">
    <h3>✅ Volume Pods</h3>
    <img src="Screenshots/Volume Pod.png" alt="Docker Runtime" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px;" />
  </div>
  <div style="flex: 1 1 45%; text-align: center;">
    <h3>✅ Exec into Volume Pod and Validate</h3>
    <img src="Screenshots/Exec into Volume Pod and Validate.png" alt="Docker Ps Output" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px;" />
  </div>
</div>


---

🚦 Execution Flow
```Task	Status
Create Minikube cluster	✅ Done
Create ConfigMap	✅ Done
Inject ConfigMap as ENV variables	✅ Done
Inject ConfigMap as Volume	✅ Done
Logs and validation screenshots	✅ Done
```
---

## ✅ Features

- 📂 Kubernetes **ConfigMap** integration
- 🌐 **Two deployment styles**: via ENV vars & via Volumes
- 📦 **Minikube local cluster** setup on MacBook M2
- 🔍 Verified via `kubectl logs` and container shell access
- 📸 Proof included through **screenshots folder**
- ✍️ Clean folder layout with `*.yaml` manifests and config

---

## 💡 Future Enhancements

- 🔁 Integrate with **GitHub Actions** for YAML linting
- 📊 Add **Prometheus + Grafana** for monitoring
- 🛡️ Extend to use **Secrets** for sensitive configs
- 🔐 RBAC policies for access control
- 📦 Convert ConfigMap to Helm Chart for scalability

---

## 🙋‍♂️ Author

**👨‍💻 Jotheeshwaran V**  
📍 Chennai, India  
📞 8667782566  
📬 [jotheeshwaran2002@gmail.com](mailto:jotheeshwaran2002@gmail.com)  
🔗 [LinkedIn](https://linkedin.com/in/jotheeshwaran-v)  
🔗 [GitHub](https://github.com/Jotheesh2002)

---

## ⚖️ License

This project is licensed under the **MIT License**.  
Feel free to ⭐ star, fork 🍴, and contribute 🛠️!
