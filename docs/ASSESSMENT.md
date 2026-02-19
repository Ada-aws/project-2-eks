# Assessment / Application Requirements

## Goal
Deploy a containerized application to Amazon EKS using:
- Terraform (EKS + networking)
- Kubernetes manifests (deployments/services)
- Helm (packaged deployment)

## What the user should be able to do
- Access the application from the internet via a Load Balancer or Ingress
- Deploy updates using Kubernetes/Helm commands
- Recreate the environment from scratch using Terraform

## MVP (Minimum Viable Product)
- EKS cluster running in a VPC
- Managed node group
- A sample app deployed (hello-world API)
- Service type `LoadBalancer` exposing it publicly

## Non-Functional Requirements
- IaC: Terraform code is modular and readable
- Security basics:
  - least privilege IAM roles
  - no secrets committed to Git
- Observability basics:
  - kubectl logs works
  - pods and nodes are visible

## Acceptance Criteria
- `terraform apply` creates cluster successfully
- `kubectl get nodes` shows nodes Ready
- `kubectl get svc` shows an external endpoint (EXTERNAL-IP or DNS)
- Application responds with HTTP 200
- `terraform destroy` cleans up resources
