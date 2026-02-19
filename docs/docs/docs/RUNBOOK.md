# Runbook (How to Run This Project)

## Prereqs
- AWS CLI configured
- Terraform installed
- kubectl installed
- Helm installed

## Create Infrastructure
1) cd terraform
2) terraform init
3) terraform apply

## Connect kubectl to the cluster
- aws eks update-kubeconfig --region us-east-1 --name <cluster-name>

## Deploy app (Kubernetes)
- kubectl apply -f k8s/

## Deploy app (Helm)
- helm install <release> helm/<chart>

## Cleanup
- terraform destroy
