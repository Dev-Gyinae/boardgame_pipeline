# Install Helm - The Kubernetes Package Manager

## What is Helm?
Helm is the package manager for Kubernetes that allows you to:
- Find and use pre-configured applications (charts)
- Share your own applications
- Manage Kubernetes manifest releases
- Simplify deployments of complex applications

## Installation Methods

### 1. Install via Script (Linux/macOS)
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
```
# Verify Installation: 
helm version

