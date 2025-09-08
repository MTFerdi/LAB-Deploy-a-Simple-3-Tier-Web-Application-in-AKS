# AKS 3-Tier Web App Lab

This lab deploys a simple 3-tier app (UI on NGINX, .NET 7 API, PostgreSQL) to Azure Kubernetes Service (AKS) using Docker + Kubernetes manifests + Ingress.

## Structure
- api/      -> .NET 7 Web API (Basic3TierAPI)
- ui/       -> Static UI served by NGINX (Basic3TierUI)
- k8s/      -> Kubernetes manifests (Deployments, Services, Ingress, PVC)

## High-Level Flow
Ingress (NGINX) -> UI (ClusterIP) -> API (ClusterIP) -> PostgreSQL (ClusterIP + PVC)
