# Deploy a Local Kubernetes Cluster Using K3s  
K3s is a lightweight Kubernetes distribution developed by Rancher Labs, packaged as a single binary under 100MB. It's ideal for local development, edge computing, and CI/CD workflows.  

**System Requirements**: Linux OS (Ubuntu/Debian recommended), 1+ vCPU, 1GB+ RAM, sudo/root access, internet connection. For production: 2+ vCPUs, 4GB+ RAM recommended.  

**Installation**: Run `curl -sfL https://get.k3s.io | sh -` to install K3s as a systemd service, set up kubectl, and create a single-node cluster with Containerd, Traefik ingress, and local storage.  

**Verification**: Check status with `sudo kubectl get nodes` (should show "Ready") and view system pods using `sudo kubectl get pods -n kube-system`.  

**kubectl Access**: Copy the kubeconfig to your user account:  
```bash
mkdir -p ~/.kube  
sudo cp /etc/rancher/k3s/k3s.yaml ~/.kube/config  
sudo chown $USER:$USER ~/.kube/config
```
