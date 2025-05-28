
# 🚀 Kubernetes Cluster on AWS with Terraform (Free Tier)

## 📘 Project Overview
This project demonstrates how to deploy a Kubernetes cluster on AWS using Terraform, host a sample application using EKS, and expose it via Ingress and Route53. The infrastructure is fully codified using Infrastructure as Code (IaC) principles, ensuring repeatable and consistent deployments.

## 🧰 Technology Stack
- **AWS EKS**: Managed Kubernetes service
- **Terraform**: Infrastructure provisioning
- **Amazon ECR**: Container image registry
- **Route 53**: DNS management
- **Docker**: Containerization
- **kubectl**: Kubernetes CLI
- **EC2**: Used as a control node for provisioning

## 🏗️ Architecture
The project follows a modern DevOps workflow:
1. Infrastructure defined using Terraform
2. Kubernetes cluster provisioned via EKS
3. Docker image built and pushed to ECR
4. Application deployed using Kubernetes manifests
5. Ingress controller exposes the app via Load Balancer
6. Load Balancer mapped to a custom domain using Route 53

## 📦 Terraform Implementation
### VPC and EKS Cluster
Terraform is used to provision:
- A custom VPC with public and private subnets
- An EKS cluster with a single t3.micro node (Free Tier eligible)
- IAM roles and security groups

## 🐳 Docker and ECR
A sample Docker image is built and pushed to Amazon ECR.

## ☸️ Kubernetes Deployment
A sample app is deployed using the following Kubernetes resources:
- **Deployment**: Runs the container
- **Service**: Exposes the app internally
- **Ingress**: Exposes the app externally via ALB

## 🌐 Route 53 Integration
The Load Balancer DNS from the Ingress is mapped to a custom domain using Route 53. A CNAME or A record is created pointing to the ALB DNS.

## ✅ Benefits of This Approach
- **Infrastructure as Code**: All resources are version-controlled
- **Free Tier Friendly**: Uses t3.micro and minimal resources
- **Scalable**: Easily extendable to multi-node clusters
- **Secure**: IAM roles and private networking
- **Automated**: Minimal manual steps after setup

## 🔮 Future Enhancements
- Add SSL using AWS Certificate Manager
- Integrate GitHub Actions or GitLab CI/CD
- Add monitoring with Prometheus and Grafana
- Use Helm for app deployment

## 📌 Conclusion
This project provides a cost-effective, scalable, and production-ready foundation for deploying containerized applications on AWS using Kubernetes and Terraform. It’s ideal for learning, prototyping, or hosting small workloads.
