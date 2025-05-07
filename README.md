# MERN Stack Deployment on Kubernetes

This repository contains Kubernetes manifests for deploying a **MERN Stack** (MongoDB, Express, React, Node.js) application on a Kubernetes cluster. The setup uses the official **MongoDB** and **Mongo Express** Docker images, with a custom Node.js Express backend and React frontend.

The purpose of this setup is to demonstrate how to deploy a MERN stack application in a **Kubernetes environment** using Kubernetes **Deployments**, **Services**, and **Secrets** for a secure and scalable infrastructure.

## Project Structure

The following files are included in this repository:

- **k8s/**
  - **mongo-deployment.yml**: Defines the deployment for MongoDB.
  - **mongo-secret.yml**: Stores MongoDB credentials as a Kubernetes secret.
  - **mongo-service.yml**: Exposes MongoDB to other services within the Kubernetes cluster.
  - **mongo-config.yml**: Stores MongoDB configuration URL in a Kubernetes ConfigMap.
  - **webapp-deployment.yml**: Defines the deployment for the Mongo Express UI.
  - **webapp-service.yml**: Exposes Mongo Express UI as a Kubernetes service.

## Prerequisites

Before you begin, you need:

1. A **Kubernetes cluster**. You can use **Minikube**, **kind**, or any other Kubernetes cluster.
2. **kubectl** installed and configured to interact with your Kubernetes cluster.
3. Docker images for **MongoDB** and **Mongo Express**.
   - The official MongoDB image is used for database services.
   - The official Mongo Express image is used for the MongoDB admin UI.

### Prerequisites Installation

1. **Install Kubernetes**:
   - For Minikube: Follow the [Minikube Installation Guide](https://minikube.sigs.k8s.io/docs/).
   - For kind: Follow the [kind Installation Guide](https://kind.sigs.k8s.io/docs/user/quick-start/).
   
2. **Install kubectl**:
   - Follow the [kubectl Installation Guide](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

3. **Install Docker** (for creating custom images or if not using official images):
   - Follow the [Docker Installation Guide](https://docs.docker.com/get-docker/).

## Setting Up the Deployment

Start by cloning the repository to your local machine:
apply the menifests:
publish the port:
go to ui and enter the credential which we store in secrets in base64 encoded form:
http://localhost:8081
Username: root
Password: root

```bash
git clone https://github.com/your-username/mern-k8s-deployment.git
cd mern-k8s-deployment

kubectl apply -f *

kubectl port-forward svc/webapp-service 8081:8081


