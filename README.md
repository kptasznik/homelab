# 🏠 Home Lab Kubernetes Cluster

![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Rocky](https://img.shields.io/badge/-Rocky%20Linux%209-%2310B981?style=for-the-badge&logo=rockylinux&logoColor=white)
![GitOps](https://img.shields.io/badge/GitOps-yellow.svg?style=for-the-badge)

A fully automated, GitOps-managed Kubernetes cluster running on Lenovo ThinkCentre hardware and Talos Linux.

## 🏗️ Infrastructure Overview

### Hardware
- Laptop MSI Bravo 17 A4DDR-088PL FHD Ryzen 5 4600H/8GB/512GB

###  Stack
- **Hypervisor**: Proxmox
- **Base OS**: Rocky Linux
- **Container Orchestration**: Kubernetes (k3s)
- **GitOps Engine**: Flux CD


## 🌟 Key Features

- **GitOps-First Approach**: All cluster configurations and applications are managed through Git using the App of Apps pattern
- **Declarative Configuration**: Everything-as-code philosophy
- **Automated Deployments**: Changes to this repository automatically sync to the cluster via Flux CD


## 🔄 Continuous Deployment

This repository uses Flux CD to automatically sync changes to the cluster. The App of Apps pattern ensures that all applications are managed consistently and can be deployed or updated with minimal manual intervention.


---

🔍 **Note**: This is a living document. As the cluster evolves, so will this documentation.

