# Kubernetes Course Labs Hackathon

Welcome to the Kubernetes Course Labs Hackathon! This project implements key Kubernetes concepts by deploying and managing infrastructure for a fictional company called **Widgetario**. It follows a structured progression from configuration to production-grade deployments.

---

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Hackathon Stages](#hackathon-stages)
  - [Part 1: Welcome to Widgetario](#part-1-welcome-to-widgetario)
  - [Part 2: Configuration](#part-2-configuration)
  - [Part 3: Storage](#part-3-storage)
  - [Part 4: Ingress](#part-4-ingress)
  - [Part 5: Productionizing](#part-5-productionizing)
  - [Part 6: Observability](#part-6-observability)
  - [Part 7: CI/CD](#part-7-cicd)
- [Sample Solutions](#sample-solutions)
- [Testing](#testing)
- [Deployment Instructions](#deployment-instructions)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This project reinforces Kubernetes skills by deploying the Widgetario app through hands-on tasks, including containerization, secrets management, persistent storage, ingress configuration, observability, and CI/CD pipeline automation.

---

## Prerequisites

- Docker
- kubectl
- Minikube or Kubernetes cluster
- Helm
- Jenkins (for CI/CD)
- Optional: Testkube for testing

---


## Hackathon Stages

### Part 1: Welcome to Widgetario

- Containerize a basic application.
- Deploy it to Kubernetes using `kubectl`.
- Expose the app using a `Service`.

### Part 2: Configuration

- Manage app settings using `ConfigMaps` and `Secrets`.
- Demonstrate separation of config and code.

### Part 3: Storage

- Use `PersistentVolumes` and `PersistentVolumeClaims`.
- Attach storage to pods for stateful services.

### Part 4: Ingress

- Install an Ingress controller (e.g., NGINX).
- Configure routing rules and enable TLS.
- Route multiple apps through one external IP.

### Part 5: Productionizing

- Add liveness/readiness probes.
- Set resource requests and limits.
- Implement pod-level security.

### Part 6: Observability

- Use Prometheus to collect metrics.
- Create dashboards in Grafana.
- Aggregate and ship logs via Fluent Bit.

### Part 7: CI/CD

- Automate builds and deployments with Jenkins.
- Integrate with GitHub Webhooks.
- Trigger deployments to Kubernetes using pipelines.

---

## Deployment Instructions

To deploy the application:

1. **Set Up Kubernetes Cluster**: Ensure your cluster is up and running.
2. **Install Helm Charts**:
   - Navigate to the `helm/` directory.
   - Run `helm install widgetario .` to deploy the application using Helm.
3. **Apply Kubernetes Manifests**:
   - Use `kubectl apply -f [manifest-file.yaml]` to apply individual Kubernetes resource definitions.
4. **Configure Ingress**:
   - Set up ingress controllers as defined in `part4-ingress/`.
   - Update DNS records or `/etc/hosts` as necessary to access the application.
5. **Set Up CI/CD Pipeline**:
   - Configure Jenkins using the provided `Jenkinsfile`.
   - Ensure Jenkins has access to the Kubernetes cluster and necessary credentials.
6. **Monitoring and Logging**:
   - Deploy Grafana and Kibana using the configurations in the `dashboards/` directory.
   - Access dashboards to monitor application performance and logs.

---

---

## Testing

Test your deployments using the provided test scripts.

### Run with Testkube


# Install Testkube
curl -sSLf https://kubeshop.github.io/testkube/install | bash

# Initialize Testkube in your cluster
testkube init

# Create and run test
testkube create test --name widgetario-test --type postman/test --uri https://github.com/Shikulisa/distributedSys-Kubernetes/tests
testkube run test widgetario-test

## Project Structure

```bash
distributedSys-Kubernetes/
├── part1-welcome/
├── part2-configuration/
├── part3-storage/
├── part4-ingress/
├── part5-productionizing/
├── part6-observability/
├── part7-ci-cd/
├── sample-solutions/
├── tests/
└── README.md
