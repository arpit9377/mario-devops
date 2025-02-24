# 🚀 Deployment of Super Mario on Kubernetes Using Terraform

## 📌 Overview
This project demonstrates how to **deploy a Super Mario application** on **AWS EKS (Elastic Kubernetes Service)** using **Terraform** for infrastructure automation. The deployment workflow includes **EC2 instances, Kubernetes, Docker, and GitHub** for version control.

## 🎯 Features
- **Infrastructure as Code (IaC)** using Terraform
- **Containerized Deployment** with Docker
- **Kubernetes Cluster Management** on AWS EKS
- **Automated Configuration** with AWS CLI & kubectl
- **CI/CD Integration** for seamless deployment

## 🏗️ Deployment Workflow

### 1️⃣ **Setup and Code Fetching**
- Developer pushes the code to **GitHub**.
- EC2 instance fetches the latest code using **GitHub Actions or manual pull**.

### 2️⃣ **Kubernetes Cluster Creation**
- **Terraform** provisions an **AWS EKS Cluster**.
- Required Terraform files: `backend.tf`, `main.tf`, `provider.tf`.

### 3️⃣ **Containerization & Deployment**
- **Docker Image** is built and tested locally.
- **Kubernetes manifest files** (`service.yaml`, `deployment.yaml`) are applied using **kubectl**.
- The application is deployed to **EKS**.

### 4️⃣ **Testing & IAM Configuration**
- Testing is done by running the container locally.
- **AWS IAM roles & policies** are set up for secure access.

## 🚀 Tech Stack
- **Infrastructure Automation**: Terraform
- **Orchestration**: Kubernetes (AWS EKS)
- **Containerization**: Docker
- **Version Control**: GitHub
- **Cloud Provider**: AWS (EC2, IAM, CLI)
- **Deployment & Management**: kubectl

## ⚡ Challenges Faced
- **Terraform Configuration**: Managing state files and backend setup.
- **IAM Permissions**: Ensuring the right access control for EKS.
- **Kubernetes Service Discovery**: Configuring `service.yaml` correctly.
- **Networking Issues**: Debugging pod communication within EKS.

## 📢 Credits & Inspiration
Big thanks to **[Aakib Khan](https://aakibkhan1.medium.com/project-6-deployment-of-super-mario-on-kubernetes-using-terraform-74c7ce79b1f6)** for the amazing guide! 🎉

## 📝 Setup & Installation
### **Prerequisites**
Ensure you have installed:
- AWS CLI
- Terraform
- Docker
- Kubernetes CLI (kubectl)

### **Installation Steps**
1. **Clone the Repository**
   ```sh
   git clone https://github.com/arpit9377/mario-devops
   cd repo-name
   ```

2. **Set Up AWS Credentials**
   ```sh
   aws configure
   ```

3. **Initialize Terraform & Create EKS Cluster**
   ```sh
   terraform init
   terraform apply -auto-approve
   ```

4. **Deploy Application on Kubernetes**
   ```sh
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml
   ```

5. **Verify Deployment**
   ```sh
   kubectl get pods
   kubectl get services
   ```

## 📝 Conclusion
This project demonstrates a **real-world deployment workflow** using **Terraform, Kubernetes, and AWS EKS**. It automates infrastructure provisioning and application deployment, making it a perfect example of **DevOps best practices**.

If you found this useful, drop a ⭐ and contribute! 🚀

