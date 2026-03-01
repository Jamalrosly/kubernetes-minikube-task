# Kubernetes Task — Minikube Namespace Setup

## Task Description
Setup Minikube locally (AWS EC2 used) and explore Kubernetes namespaces.

## Tech Stack Used
- AWS EC2 (Ubuntu t2.medium)
- Docker
- kubectl
- Minikube
- Kubernetes

## Steps Performed

### 1. Installed Docker
Verified using:
docker run hello-world

### 2. Installed kubectl
Verified using:
kubectl version --client

### 3. Installed Minikube and started cluster
Commands:
minikube start --driver=docker
minikube status
kubectl get nodes

### 4. Explored Default Namespaces
kubectl get ns

### 5. Created Namespaces
kubectl create namespace dev
kubectl create namespace test

### 6. Deployment in dev namespace
kubectl create deployment nginx-dev -n dev --image=nginx
kubectl get pods -n dev

### 7. Deployment in test namespace
kubectl create deployment nginx-test -n test --image=nginx
kubectl get pods -n test

### 8. Namespace Isolation Proof
kubectl get pods --all-namespaces

## Output Screenshots
All output screenshots available in screenshots folder.

