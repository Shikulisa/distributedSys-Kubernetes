# 🚀 Kubernetes Course Labs Hackathon

Welcome to the **Kubernetes Course Labs Hackathon**! This hands-on project is your opportunity to apply the Kubernetes skills you've acquired throughout the course by deploying and managing a real-world application. You'll encounter challenges, troubleshoot issues, and deepen your understanding of Kubernetes concepts.([Kubernetes Course Labs][1])

---

## 📚 Table of Contents

* [Overview](#overview)
* [Prerequisites](#prerequisites)
* [Project Structure](#project-structure)
* [Hackathon Parts](#hackathon-parts)

  * [Part 1: Deploying Widgetario](#part-1-deploying-widgetario)
  * [Part 2: Configuration Management](#part-2-configuration-management)
  * [Part 3: Storage Solutions](#part-3-storage-solutions)
  * [Part 4: Health Checks](#part-4-health-checks)
  * [Part 5: Scaling and Load Balancing](#part-5-scaling-and-load-balancing)
  * [Part 6: Ingress and TLS](#part-6-ingress-and-tls)
  * [Part 7: CI/CD Pipeline](#part-7-cicd-pipeline)
* [Sample Solutions](#sample-solutions)
* [Contributing](#contributing)
* [License](#license)

---

## 📝 Overview

The Hackathon revolves around **Widgetario**, a fictional company specializing in gadget sales. Your mission is to deploy their multi-component web application onto a Kubernetes cluster. The application components are containerized and available on Docker Hub.([Kubernetes Course Labs][1])

You'll progress through multiple stages, each introducing new Kubernetes concepts and challenges:([Opsgility][2])

1. Deploying the application components.
2. Managing configurations securely.
3. Implementing storage solutions.
4. Setting up health checks.
5. Scaling services and load balancing.
6. Configuring ingress and TLS.
7. Establishing a CI/CD pipeline.

Each part builds upon the previous, enhancing the application's robustness and scalability.

---

## 🔧 Prerequisites

Before you begin, ensure you have the following:

* A running Kubernetes cluster (e.g., Minikube, Docker Desktop, or a cloud provider).
* `kubectl` configured to interact with your cluster.
* Basic understanding of Kubernetes concepts: Pods, Deployments, Services, ConfigMaps, Secrets, Volumes, Ingress, etc.
* Familiarity with YAML syntax.([GitHub][3])

---

* `hackathon/`: Contains directories for each part of the Hackathon and their respective manifests.
* `labs/`: Additional lab exercises to reinforce Kubernetes concepts.
* `scripts/`: Utility scripts for setup and management.
* `setup/`: Cluster setup configurations and instructions.([GitHub][4], [Medium][5])

---

## 🧩 Hackathon Parts

### Part 1: Deploying Widgetario

Begin by deploying the core components of the Widgetario application:([Kubernetes Course Labs][1])

* `products-db`: PostgreSQL database.
* `products-api`: Java-based API service.
* `stock-api`: Go-based API service.
* `web`: .NET Core frontend application.([Kubernetes Course Labs][1])

Use the provided architecture diagram to model your Kubernetes manifests. Ensure each component is deployed with appropriate Services and Deployments.([Kubernetes Course Labs][1])

### Part 2: Configuration Management

Enhance security and flexibility by externalizing configurations:

* Use Secrets to manage sensitive data like database passwords.
* Implement ConfigMaps for non-sensitive configurations.
* Override default configurations in container images.([Kubernetes Course Labs][1])

Investigate each component to determine the appropriate configuration strategy.

### Part 3: Storage Solutions

Implement storage strategies for application components:

* Use `emptyDir` volumes for caching mechanisms in `stock-api`.
* Deploy PersistentVolumes and PersistentVolumeClaims for `products-db` to ensure data persistence.([Kubernetes Course Labs][1])

Model the storage requirements in your manifests accordingly.

### Part 4: Health Checks

Ensure application reliability by configuring health probes:

* Define `readinessProbe` and `livenessProbe` for each component.
* Use appropriate endpoints and response criteria to assess application health.

These probes help Kubernetes manage application availability and recovery.

### Part 5: Scaling and Load Balancing

Optimize application performance and availability:

* Configure Horizontal Pod Autoscalers (HPA) based on CPU utilization.
* Set up Services with appropriate types (`ClusterIP`, `NodePort`, or `LoadBalancer`) to distribute traffic.

Test scaling behavior under simulated load conditions.

### Part 6: Ingress and TLS

Manage external access and secure communication:

* Deploy an Ingress Controller (e.g., NGINX Ingress Controller).
* Define Ingress resources to route traffic to services.
* Implement TLS certificates for secure HTTPS communication.

Ensure domain names and certificates are correctly configured.

### Part 7: CI/CD Pipeline

Automate application deployment and updates:

* Set up a CI/CD pipeline using tools like Jenkins, GitHub Actions, or Argo CD.
* Automate build, test, and deployment processes.
* Implement version control and rollback mechanisms.([Kubernetes Course Labs][6])

Ensure the pipeline integrates seamlessly with your Kubernetes cluster.

---

## 🧪 Sample Solutions

If you encounter challenges or wish to compare your implementation, sample solutions are available:([Kubernetes Course Labs][1])

```bash
kubectl apply -f hackathon/solutions/part-1/
kubectl apply -f hackathon/solutions/part-2/
# ... and so on for each part
```



These solutions provide reference implementations for each Hackathon part.([Kubernetes Course Labs][7])

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions, improvements, or additional exercises, feel free to fork the repository and submit a pull request.

---

Happy hacking! 🚀

---

For more information and resources, visit the [Kubernetes Course Labs Hackathon page](https://kubernetes.courselabs.co/hackathon/).

---

[1]: https://kubernetes.courselabs.co/hackathon/?utm_source=chatgpt.com "Hackathon! | Kubernetes Course Labs"
[2]: https://opsgility.com/advanced-kubernetes-microsoft-cloud-hack?utm_source=chatgpt.com "Advanced Kubernetes Hackathon​ | Azure Training - Opsgility"
[3]: https://github.com/piouson/kubernetes-bootcamp?utm_source=chatgpt.com "Kubernetes Bootcamp (CKAD) - GitHub"
[4]: https://github.com/courselabs/kubernetes?utm_source=chatgpt.com "Labs and exercises to help you learn Kubernetes. - GitHub"
[5]: https://medium.com/%40ramu.allam100/write-up-hacking-securing-kubernetes-cluster-the-offensive-labs-564a723e7f5e?utm_source=chatgpt.com "Review: “Hacking & Securing Kubernetes Clusters” course by The ..."
[6]: https://kubernetes.courselabs.co/?utm_source=chatgpt.com "Kubernetes Course Labs | Labs and exercises to help you learn ..."
[7]: https://kubernetes.courselabs.co/hackathon/solution-part-7/?utm_source=chatgpt.com "Hackathon Part 7 Solution | Kubernetes Course Labs"
