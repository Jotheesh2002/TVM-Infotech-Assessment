<h1 align="center">
  🚀 Kubernetes ConfigMap Demo
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Kubernetes-v1.33-blue?style=for-the-badge&logo=kubernetes" />
  <img src="https://img.shields.io/badge/Minikube-Running-brightgreen?style=for-the-badge&logo=linux" />
  <img src="https://img.shields.io/badge/MacBook-Air%20M2-lightgrey?style=for-the-badge&logo=apple" />
</p>

<p align="center">
  <strong>✨ TVM Infotech Task Submission ✨</strong><br>
  <i>Created with ❤️ by Jotheesh V | Assigned by Yogi Mam (HR)</i>
</p>

---

## 📚 Table of Contents

- [📌 About](#-about)
- [📁 Project Structure](#-project-structure)
- [🛠️ Setup Instructions](#️-setup-instructions)
- [🚦 Execution Flow](#-execution-flow)
- [📸 Screenshots](#-screenshots)
- [📬 Contact](#-contact)

---

## 📌 About

This project demonstrates the use of **Kubernetes ConfigMaps** to inject application configuration into pods. Two methods are shown:

- As **environment variables**
- As **mounted volumes**

> 💼 Task Assigned by: **TVM Infotech Pvt. Ltd.**
>  
> 🧑‍🏫 Supervisor: **Yogi Mam (HR)**  
> 🗓️ Completed on: August 2025

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

🚦 Execution Flow
Task	Status
Create Minikube cluster	✅ Done
Create ConfigMap	✅ Done
Inject ConfigMap as ENV variables	✅ Done
Inject ConfigMap as Volume	✅ Done
Logs and validation screenshots	✅ Done

📸 Screenshots
All screenshots are provided inside the screenshots/ folder

Description	Preview
✅ Minikube Started	
✅ ConfigMap Created	
✅ Pod using Env Variables	
✅ Pod using Volume Mount	
✅ ConfigMap Values inside Container	

📦 Note: Replace the image paths above with your actual screenshot names inside screenshots/

🧠 Fun Fact
ConfigMaps are like environment notes 📋 Kubernetes reads every time it runs your pod!

📬 Contact
If you'd like to connect:

📧 Email: jotheeshv@example.com (replace with your actual email)

💼 LinkedIn: linkedin.com/in/jotheeshv (if applicable)

📂 GitHub: github.com/your-username

<p align="center"> Made with ❤️ for TVM Infotech Pvt. Ltd. </p> ```
