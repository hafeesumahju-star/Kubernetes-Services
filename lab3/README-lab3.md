# Lab 3 – Ingress with NGINX Ingress Controller

Student: Azeem

## Objective

Demonstrate how an Ingress resource uses the NGINX Ingress Controller to route HTTP traffic to a ClusterIP Service in front of a sample application, and show real browser access via an SSH tunnel.

## 1. Sample App Deployment

- File: `app-deployment.yaml`
- Deployment:
  - Name: `sample-app`
  - Replicas: 2
  - Label: `app: sample-app`
- Commands:
  ```bash
  kubectl apply -f app-deployment.yaml
  kubectl get pods -o wide
