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


## 📦 Part 1: Welcome to Widgetario

Containerize and deploy the base Widgetario application to Kubernetes using **Deployments** and **Services**.

---

## ⚙️ Part 2: Configuration

Use **ConfigMaps** and **Secrets** to manage environment-specific settings and sensitive data securely.

---

## 💾 Part 3: Storage

Implement **PersistentVolumes (PVs)** and **PersistentVolumeClaims (PVCs)** for persistent application storage.

---

## 🌐 Part 4: Ingress

Set up an **Ingress Controller** to:
- Route external traffic.
- Secure communication using **TLS** certificates.

---

## 🏗️ Part 5: Productionizing

Make your deployment production-ready by:
- Adding **readiness** and **liveness probes**.
- Following **security best practices**.
- Defining **resource limits** for containers.

---

## 📊 Part 6: Observability

Enable monitoring and logging by:
- Integrating **Prometheus** and **Grafana** for performance metrics.
- Collecting logs and application metrics.

---

## 🔁 Part 7: CI/CD

Automate your pipeline using **Jenkins**:
- Trigger builds, tests, and deployments on each GitHub push.
- Use a properly configured `Jenkinsfile`.

---

## 🧪 Testing with Testkube

Ensure your services are working as expected:

### Install and initialize Testkube:

```bash
curl -sSLf https://kubeshop.github.io/testkube/install | bash
testkube init
