WordPress on AWS EKS – Production-Style Deployment
📌 Project Overview

This project demonstrates how to deploy a scalable WordPress application on Amazon EKS using Infrastructure as Code and Kubernetes best practices.

Instead of running WordPress on a single EC2 instance, this architecture uses Kubernetes to enable high availability, auto-scaling, and self-healing workloads.

❓ Problem

Running WordPress on a single EC2 instance introduces:

Single point of failure

No automatic scaling

Manual patching and upgrades

Downtime during deployments

This project solves those limitations by containerizing WordPress and deploying it on a managed Kubernetes cluster (EKS).

🏗 Architecture Built

Infrastructure is provisioned using Terraform.

The deployed architecture includes:

Amazon EKS cluster

Kubernetes Deployments for WordPress

Kubernetes Service for networking

Horizontal Pod Autoscaler (HPA)

MariaDB deployed as a StatefulSet

Kubernetes Namespaces for isolation

Helm for packaging

📈 Scaling Strategy

WordPress runs as multiple replicas

HPA automatically scales pods based on CPU usage

Kubernetes restarts failed containers automatically

Rolling updates prevent downtime

🗃 Why StatefulSet for MariaDB?

Databases require:

Persistent storage

Stable network identity

Ordered startup/shutdown

StatefulSets guarantee data stability and identity consistency across pod restarts.

⚙️ Tools Used

AWS (EKS)

Kubernetes

Terraform

Helm

Docker

Git & GitHub

🚀 How to Deploy

Provision infrastructure with Terraform

terraform init
terraform apply

Configure kubectl to connect to EKS

Deploy Kubernetes manifests

kubectl apply -f k8s/

Verify deployment

kubectl get pods
kubectl get svc
🎯 What I Learned

Designing scalable container-based systems

Difference between stateless and stateful workloads

Auto-scaling strategies in Kubernetes

Infrastructure as Code best practices

Production-ready deployment patterns

💼 Author

Adama Sannoh
Cloud Engineer | AWS & KubernetesCgit 