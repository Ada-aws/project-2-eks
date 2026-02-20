Your README.md Must Tell a Story

Your README should answer:

What is this project?

What problem does it solve?

What architecture did you build?

What tools were used?

How to deploy it?

What you learned

If someone only reads README.md,
they should understand your entire project.

2️⃣ Make Sure Your Repo Shows This Structure (Clean)
project-2-eks/
│
├── docs/
│   ├── ARCHITECTURE.md
│   ├── DECISIONS.md
│   ├── ASSESSMENT.md
│   └── RUNBOOK.md
│
├── terraform/
│   └── main.tf
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── hpa.yaml
│
├── helm/
│   └── Chart.yaml
│
└── README.md

If you have that?

You are not a beginner anymore.
You’re building like an engineer.

Now Let Me Be Real With You

You keep thinking:
“If I just finish it and push it, I’m done.”

No.

You are done when you can:

Explain Kubernetes to a 5th grader

Explain EKS in an interview

Draw your architecture on a whiteboard

Explain scaling

Explain why HPA

Explain why StatefulSet

That’s when you’re dangerous.

Let Me Ask You This

If someone asked:

Why didn’t you just run WordPress on one EC2?

Could you confidently answer without freezing?

If not — that’s what we fix next.

Here’s What We’re Doing

We are NOT moving forward until:

You can explain your entire Project 2 in this format:

Problem

Solution

Architecture

Scaling

Why Kubernetes

Why EKS

Why HPA

Why Namespace

Why StatefulSet

Challenges

Improvements

When you can say that smoothly?

You’re interview ready.

So no.
You’re not “just uploading a job”.

You are building a Cloud Engineer portfolio asset.

Now tell me:

Do you want to polish the README first
or do you want me to drill you like an interviewer?

PUSH README FIRST

YESSSS 🔥
That’s engineer energy.

We’re going to push a README that makes recruiters pause.

Not basic.
Not “I deployed EKS”.

We’re writing it like a Cloud Engineer.

🧠 Step 1 — Replace Your README.md With This

Open your README.md in VS Code.

Delete everything.

Paste this:

🚀 Project 2 – WordPress on AWS EKS (Production-Style Deployment)
📌 Project Overview

This project demonstrates how to deploy a scalable WordPress application on Amazon EKS (Elastic Kubernetes Service) using Infrastructure as Code and Kubernetes best practices.

Instead of running WordPress on a single EC2 instance, this project uses Kubernetes to enable:

High availability

Auto-scaling

Self-healing containers

Production-style deployment patterns

❓ Problem Statement

Running WordPress on a single EC2 instance creates:

❌ Single point of failure

❌ No auto-scaling

❌ Manual infrastructure management

❌ Difficult upgrades

This project solves those problems using Kubernetes and AWS-managed services.

🏗 Architecture

The infrastructure is provisioned using Terraform and deployed to AWS.

Components:

Amazon EKS Cluster

Kubernetes Deployments

Kubernetes Services

Horizontal Pod Autoscaler (HPA)

MariaDB (StatefulSet)

Namespaces for isolation

Helm (for package management)

⚙️ Technologies Used

AWS EKS

Kubernetes

Terraform

Helm

Docker

GitHub

📂 Repository Structure
project-2-eks/
│
├── docs/
│   ├── ARCHITECTURE.md
│   ├── DECISIONS.md
│   ├── ASSESSMENT.md
│   └── RUNBOOK.md
│
├── terraform/
│   └── main.tf
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── hpa.yaml
│
├── helm/
│   └── Chart.yaml
│
└── README.md
📈 Scaling Strategy

This project uses:

Horizontal Pod Autoscaler (HPA) to scale WordPress pods based on CPU usage

Kubernetes self-healing to automatically restart failed containers

Multiple replicas for high availability

🗃 Why MariaDB as a StatefulSet?

Databases require:

Persistent storage

Stable network identity

Ordered startup and shutdown

A StatefulSet ensures the database maintains its data and identity even if pods restart.

🎯 Key Learning Outcomes

Understanding Kubernetes architecture

Deploying workloads on EKS

Implementing auto-scaling strategies

Managing stateful vs stateless applications

Infrastructure as Code using Terraform

🚀 Future Improvements

Add CI/CD pipeline using GitHub Actions or Jenkins

Implement monitoring with Prometheus & Grafana

Use AWS Load Balancer Controller

Add Secrets Manager integration

Implement production-grade security hardening

💡 Author

Adama Sannoh                                                                                       Cloud Engineer | AWS & Kubernetes Focused
Infrastructure as Code • Scalable Systems • Production-Ready Deployments