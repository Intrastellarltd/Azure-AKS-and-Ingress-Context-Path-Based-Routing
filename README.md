# Azure AKS and Ingress Nginx - Context Path Based Routing

## Architecture Diagram

![Azure AKS and Ingress Nginx - Context Path Based Routing](architecture%20diagram/Azure%20AKS%20and%20Ingress%20–%20Context%20Path%20Based%20Routing%20-%2020112023.drawio.png)

---

## Problem Statement

Managing multiple web applications within a Kubernetes cluster can become complex, especially when each application requires its own deployment, service, and configurations. In addition, exposing these applications to external traffic efficiently while maintaining a clear structure can be challenging. Traditional load balancers often lack the flexibility needed for intricate routing configurations.

## Solution

This repo addresses these challenges by demonstrating how to implement Context Path Based Routing using Ingress in Azure AKS. Context Path Based Routing allows you to route incoming traffic to different services based on the path of the URL. This not only simplifies the management of multiple applications but also enhances the overall accessibility and organization of your services.

## Key Features

- **Web App Deployment Simplification**: We provide Kubernetes manifest files for three web applications, each with its deployment and service configurations.

- **MySQL Integration**: A comprehensive setup for a web application with MySQL, including a persistent volume claim (PVC), configuration map, deployment, service, and secret management.

- **Ingress for Context Path Based Routing**: Ingress Nginx to efficiently route traffic based on context paths, making it easier to expose multiple services through a single entry point.

---

### Deploy and Verify

```shell
k apply -R -f kube-manifests/

k get pods

k get svc

k get ingress

k get all
```

---

### Destroy and Clean-up

```shell
k delete -f kube-manifests/
```
