# ☸️ Amazon EKS Kubernetes Deployment

A hands-on DevOps project demonstrating containerized application deployment on Kubernetes / Amazon EKS with Docker, Kubernetes manifests, LoadBalancer service, and Horizontal Pod Autoscaling.

## 🚀 Project Overview

This project demonstrates how a containerized web application can be deployed and managed on Amazon EKS.

The application runs using Nginx and is packaged as a Docker container.

## 🛠️ Technologies Used

- AWS
- Amazon EKS
- Kubernetes
- Docker
- Nginx
- Horizontal Pod Autoscaler (HPA)
- Git & GitHub

## 🏗️ Architecture

Developer  
↓  
GitHub Repository  
↓  
Docker Image  
↓  
Container Registry  
↓  
Amazon EKS  
↓  
Kubernetes Deployment  
↓  
Pods  
↓  
LoadBalancer Service  
↓  
Application

## 📁 Project Structure

    eks-kubernetes-deployment/
    ├── Dockerfile
    ├── index.html
    ├── namespace.yaml
    ├── deployment.yaml
    ├── service.yaml
    ├── hpa.yaml
    └── README.md

## 🐳 Docker

The application uses an Nginx Alpine image.

Build the Docker image:

    docker build -t ravi-devops-app .

Tag the image:

    docker tag ravi-devops-app:latest YOUR_DOCKERHUB_USERNAME/ravi-devops-app:latest

Push the image:

    docker push YOUR_DOCKERHUB_USERNAME/ravi-devops-app:latest

## ☸️ Kubernetes Deployment

Create the namespace:

    kubectl apply -f namespace.yaml

Deploy the application:

    kubectl apply -f deployment.yaml

Create the LoadBalancer service:

    kubectl apply -f service.yaml

Configure autoscaling:

    kubectl apply -f hpa.yaml

## 🔍 Verify Deployment

Check pods:

    kubectl get pods -n ravi-devops

Check deployment:

    kubectl get deployments -n ravi-devops

Check service:

    kubectl get svc -n ravi-devops

Check HPA:

    kubectl get hpa -n ravi-devops

## 📈 Horizontal Pod Autoscaling

The HPA configuration automatically scales the application based on CPU utilization.

- Minimum replicas: 2
- Maximum replicas: 5
- Target CPU utilization: 60%

> Kubernetes Metrics Server is required for CPU-based HPA metrics.

## 🔄 Deployment Flow

Code  
↓  
Docker Build  
↓  
Container Registry  
↓  
Amazon EKS  
↓  
Kubernetes Deployment  
↓  
LoadBalancer  
↓  
Application  
↓  
Horizontal Pod Autoscaling

## 🔐 Best Practices

- Use Kubernetes namespaces for workload isolation
- Avoid storing credentials in source code
- Use versioned Docker image tags for production deployments
- Configure resource requests and limits
- Use Kubernetes Secrets for sensitive configuration
- Monitor application and cluster health

## 📌 Future Improvements

- Helm Chart deployment
- AWS ECR integration
- GitHub Actions CI/CD
- Kubernetes Ingress
- AWS Load Balancer Controller
- ConfigMaps and Secrets
- Prometheus & Grafana monitoring
- Rolling deployment strategy

## 👨‍💻 Author

**Ravi Babu**  
DevOps Engineer | AWS | Kubernetes | Terraform | CI/CD
