# 🚀 NoteVault: DevOps-Powered Todo Application

A production-grade Todo application demonstrating modern DevOps practices, complete with CI/CD pipelines, security scanning, and multiple deployment options. This project serves as both a practical application and a comprehensive showcase of DevOps best practices including containerization, infrastructure as code, automated testing, and cloud deployment strategies.

**Tech Stack:**
- 🔧 **Backend:** Node.js, Express.js
- 🎨 **Frontend:** EJS Templates, CSS
- 🗄️ **Database:** File System (for simplicity)
- 🐳 **Container:** Docker, Docker Compose
- ☸️ **Orchestration:** Kubernetes, GKE Autopilot
- 🔄 **CI/CD:** Jenkins, Azure Pipelines
- 🏗️ **IaC:** Terraform
- 🔒 **Security:** SonarQube, OWASP, Trivy
- 🧪 **Testing:** npm test suite

## 🎯 Project Overview

This project demonstrates:
- End-to-end DevOps pipeline implementation
- DevSecOps practices with integrated security scanning
- Multiple deployment strategies (Docker, Kubernetes, Cloud)
- Infrastructure as Code with Terraform
- Continuous Integration with Jenkins and Azure Pipelines
- Cloud-native deployment on GKE Autopilot

## 🌟 Features

- Simple and intuitive Todo list application
- Multiple deployment options (Docker, Kubernetes, Terraform)
- Comprehensive CI/CD pipelines (Jenkins, Azure Pipelines)
- Security scanning and best practices
- Infrastructure as Code implementations

## 🚀 Quick Start

### Local Development Setup

1. Install dependencies:

```bash
sudo apt install nodejs
sudo apt install npm
npm install
```

2. Run the application:
```bash
node app.js
```

### Docker Deployment

Run using Docker Compose:
```bash
docker-compose up -d
```

The application will be available at `http://localhost:8000`

## 🛠️ Deployment Options

### 1. Docker Container
- Built using Node.js 12.2.0-alpine base image
- Exposed on port 8000
- Automated tests run during build process
- Available on DockerHub: `trainwithshubham/node-app:latest`

### 2. Kubernetes Deployment
The application can be deployed to Kubernetes using the provided manifests in the `k8s` directory:

- `pod.yml` - Basic pod configuration
- `deployment.yml` - Deployment with 2 replicas and resource limits
- `service.yml` - NodePort service configuration
- `replica-sets.yml` - ReplicaSet configuration for scaling

Deploy using:
```bash
kubectl apply -f k8s/
```

### 3. Terraform Infrastructure
Terraform configurations are available for automated infrastructure provisioning:

- Docker container deployment
- Provider configuration
- Resource definitions

Deploy using:
```bash
cd terraform
terraform init
terraform apply
```

## 🔄 CI/CD Pipelines

### Jenkins Pipeline
The Jenkinsfile includes stages for:
1. Code Clone
2. Code Build & Test
3. Push to DockerHub
4. Deployment

### Azure Pipelines
Basic Azure pipeline configuration available for:
- Building
- Testing
- Deployment

## 🔒 DevSecOps Implementation

Complete DevSecOps toolchain integration including:

- SonarQube for code quality analysis
- OWASP dependency check
- Trivy for container scanning
- Quality gates implementation

### Security Tools Setup

1. SonarQube:
```bash
docker run -itd --name sonarqube-server -p 9000:9000 sonarqube:lts-community
```

2. Required Jenkins Plugins:
- SonarQube Scanner
- Sonar Quality Gates
- OWASP Dependency-Check
- Docker Plugin

## 🌐 Cloud Deployment

### Google Kubernetes Engine (GKE) Autopilot

The application supports deployment on GKE Autopilot with Kustomize:

1. Install HELM:
```bash
helm repo add helm https://helm.sh/helm
helm repo update
```

2. Setup nginx-controller:
```bash
helm repo add nginx https://kubernetes.github.io/ingress-nginx
helm repo update
helm install nginx nginx/ingress-nginx
```

## 📝 Application Structure

The application uses:
- EJS templating engine for views
- RESTful routes for todo operations
- Responsive UI with modern styling
- CRUD operations for todo items
