# Online App

A containerized web application used for hands-on Kubernetes and DevOps practice.

## Overview

This repository contains the **Online App** along with the Kubernetes configuration used to deploy and manage it.

The application code is based on the existing project, while my work in this repository is focused primarily on the **Kubernetes infrastructure and deployment configuration**.

The purpose of the project is to gain practical experience with Kubernetes by configuring the application from deployment through networking and autoscaling.

## Kubernetes

The `k8/` directory contains the Kubernetes manifests used for the application.

The setup includes:

* Namespace
* ConfigMap
* Secrets
* Deployment
* Service
* Ingress
* Horizontal Pod Autoscaler (HPA)

### Application Flow

```text
                    Client
                      |
                      v
                 NGINX Ingress
                      |
                      v
                   Service
                      |
              +-------+-------+
              |               |
              v               v
           Pod 1           Pod 2
              |               |
              +-------+-------+
                      |
                      v
               Application
```

## Kubernetes Resources

### Deployment

Manages the application Pods and maintains the desired number of replicas.

### Service

Provides stable networking and exposes the application Pods within the Kubernetes cluster.

### ConfigMap

Stores non-sensitive configuration required by the application.

### Secrets

Stores sensitive configuration separately from the application configuration.

### Ingress

Routes external HTTP traffic to the application Service using the NGINX Ingress Controller.

### HPA

The Horizontal Pod Autoscaler is configured to practice automatic Pod scaling based on resource utilization.

## Repository Structure

```text
Online-app/
├── k8/
│   ├── namespace.yml
│   ├── configmap.yml
│   ├── secret.yml
│   ├── deployment.yml
│   ├── service.yml
│   ├── ingress.yml
│   ├── hpa.yml
│   └── ...
│
├── src/
├── public/
├── docker-compose.yml
├── package.json
└── README.md
```

## Technologies

* Docker
* Kubernetes
* NGINX Ingress Controller
* YAML
* Git
* GitHub

## Current Focus

This project is currently being used to practice Kubernetes rather than to make major changes to the application itself.

The main changes I have made are within the Kubernetes configuration, including deployment, services, configuration, Ingress, and autoscaling.

This work is part of my ongoing DevOps learning path.

## Next Step

The next stage of this project is **Terraform**.

The goal is to move from manually managed Kubernetes resources toward Infrastructure as Code and eventually integrate the project with CI/CD and cloud infrastructure.

```text
Docker
   ↓
Kubernetes
   ↓
Ingress & HPA
   ↓
Terraform
   ↓
CI/CD
   ↓
Cloud Infrastructure





<img width="1920" height="1080" alt="Screenshot from 2026-09-12 17-02-47" src="https://github.com/user-attachments/assets/79ec3780-16bf-4192-aa2d-c1f07200aad3" />




<img width="1920" height="1080" alt="Screenshot from 2026-09-12 13-41-02" src="https://github.com/user-attachments/assets/fbeb1054-04ad-4640-b18f-ca6f82b536d3" />



<img width="1920" height="1080" alt="Screenshot from 2026-09-11 17-12-58" src="https://github.com/user-attachments/assets/3626de59-0840-4fac-b2ae-31478beeec03" />
