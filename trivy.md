# Install and Use Trivy for Container Vulnerability Scanning  
Trivy is a comprehensive open-source vulnerability scanner for containers and other artifacts. To install on Linux/macOS:  

**Installation**:  
```bash
# Linux (deb/rpm)
sudo apt-get install wget apt-transport-https gnupg lsb-release
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy

# macOS (Homebrew)
brew install aquasecurity/trivy/trivy
```
# Basic Scanning:
Scan a Docker image:
```bash
    trivy image [YOUR_IMAGE]  # e.g. trivy image nginx:latest
```
