# EKS Architecture Overview

## Goal
Provision a production-style Amazon EKS cluster using Terraform
and deploy workloads using Kubernetes manifests and Helm charts.

## High-Level Components

1. VPC (Virtual Private Cloud)
2. Public and Private Subnets
3. Internet Gateway
4. NAT Gateway
5. EKS Cluster
6. Node Groups
7. Kubernetes Workloads
8. Helm for application packaging

## Flow

User → Internet → Load Balancer → EKS → Pods → Services
