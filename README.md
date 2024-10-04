# Nginx Ansible Role 📦🛠️

This project provides an Ansible role for installing and configuring **Nginx** on various hosts. 

## Overview

The Nginx Ansible role streamlines the process of installing Nginx on managed nodes. It allows system administrators to deploy and configure Nginx quickly, improving efficiency and reducing the chance of human error. 

## Getting Started

### Installing Ansible

```bash
- sudo apt update
- sudo apt install pipx
- pipx ensurepath
- pipx install --include-deps ansible
- pipx install ansible-core
- pipx upgrade --include-injected ansible
- pipx inject ansible argcomplete
- pipx inject --include-apps ansible argcomplete
```

### Setting Up SSH 🔑

1. Change the IP address in the inventory.
2. Generate a new SSH key:
   ```bash
   - ssh-keygen -t ed25519 -C "ansible"
   ```
3. Copy the public key to the managed node:
   ```bash
   - ssh-copy-id -i ../.ssh/ansible <IP_Address>
   ```
4. Test the connection:
   ```bash
   - ssh -i ../.ssh/ansible <IP_Address>
   ```
5. Verify that everything is set up correctly:
   ```bash
   - ansible all -m ping
   ```

### Testing Installation ✅

1. Check if Nginx is installed:
   ```bash
   - which nginx
   ```
2. Verify Nginx is running:
   ```bash
   - systemctl status nginx
   ```
3. Test Nginx with curl:
   ```bash
   - curl http://localhost
   ```
