# 🏠 Home Lab Kubernetes Cluster

![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Rocky](https://img.shields.io/badge/-Rocky%20Linux%209-%2310B981?style=for-the-badge&logo=rockylinux&logoColor=white)
![GitOps](https://img.shields.io/badge/GitOps-yellow.svg?style=for-the-badge)

A fully automated, GitOps-managed Kubernetes cluster running on Proxmox and Rocky Linux VMs.

## 🏗️ Infrastructure Overview

### Hardware
- Laptop MSI Bravo 17 A4DDR-088PL FHD Ryzen 5 4600H/32GB/512GB

###  Stack
- **Hypervisor**: Proxmox
- **Base OS**: Rocky Linux
- **Container Orchestration**: Kubernetes (k3s)
- **GitOps Engine**: Flux CD

## 💻 Virtual Machine Architecture

The infrastructure consists of multiple virtual machines provisioned in Proxmox and categorized by role:

### 🧩 Kubernetes Cluster (K3s)
- **k3s-master-01** – Control plane node running Kubernetes API server, controller-manager, scheduler, and etcd (or external DB)
- **k3s-worker-01, k3s-worker-02, k3s-worker-03** – Worker nodes that host all pods and workloads

All K3s nodes run **Rocky Linux** and were joined to the cluster using `k3sup`. The setup uses **Traefik** as an ingress controller and loadbalancer, and uses GitOps for full automation.

## 🌟 Key Features

- **GitOps-First Approach**: All cluster configurations and applications are managed through Git using the App of Apps pattern
- **Declarative Configuration**: Everything-as-code philosophy
- **Automated Deployments**: Changes to this repository automatically sync to the cluster via Flux CD


## 🔄 Continuous Deployment

This repository uses Flux CD to automatically sync changes to the cluster. The App of Apps pattern ensures that all applications are managed consistently and can be deployed or updated with minimal manual intervention.


---

🔍 **Note**: This is a living document. As the cluster evolves, so will this documentation.
