# Kubernetes Nginx Deployment

## Project Overview

This project demonstrates deploying a containerized Nginx web application on Kubernetes using Deployments, Services, and ConfigMaps.

The application runs with multiple replicas and is exposed through a Kubernetes NodePort Service.

---

## Architecture

User Browser
↓
NodePort Service
↓
Deployment
↓
3 Replica Pods
↓
Nginx Container

---

## Technologies Used

* Kubernetes
* Docker
* Nginx
* YAML
* Docker Desktop Kubernetes

---

## Kubernetes Components

### Deployment

The Deployment manages the lifecycle of the Nginx Pods and ensures the desired number of replicas are always running.

### Pods

The application runs with 3 replicas to provide high availability.

### Service

A NodePort Service exposes the application outside the Kubernetes cluster.

### ConfigMap

The custom HTML page is stored in a ConfigMap and mounted into the Nginx container.

---

## Deployment Commands

Apply Deployment

```bash
kubectl apply -f deployment.yaml
```

Apply Service

```bash
kubectl apply -f service.yaml
```

Apply ConfigMap

```bash
kubectl apply -f configmap.yaml
```

Verify Resources

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

Restart Deployment

```bash
kubectl rollout restart deployment nginx-deployment
```

---

## Project Output

The application displays a custom Kubernetes project page hosted through Nginx and managed by Kubernetes.

---

## Screenshots

### Application Page

![Application](screenshots/application-page.png)

### Running Pods

![Pods](screenshots/running-pods.png)

### Service Configuration

![Service](screenshots/service-output.png)

---

## Author

Kauushik Selvan

LinkedIn:
[www.linkedin.com/in/kauushik](http://www.linkedin.com/in/kauushik)

GitHub:
https://github.com/Kauushik
