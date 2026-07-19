# Ansible Automation Demo

## Project Overview

This project demonstrates Infrastructure Automation using Ansible. It automates server configuration, software installation, and application deployment on remote Linux servers using Ansible playbooks.

The project follows Infrastructure as Code (IaC) principles by eliminating manual server configuration and ensuring consistent deployments across multiple hosts.

---

# Architecture Diagram

```text
                 Developer
                      |
                  GitHub Repository
                      |
                 Jenkins Pipeline
                      |
                  Ansible Control Node
                      |
             -------------------------
             |                       |
        Managed Node 1         Managed Node 2
          (Web Server)          (Application Server)
             |                       |
        Automated Configuration via SSH
```

---

# Objectives

- Automate Linux server configuration.
- Eliminate repetitive manual administration tasks.
- Demonstrate Configuration Management using Ansible.
- Deploy applications consistently across multiple servers.
- Showcase Infrastructure as Code (IaC) best practices.
- Integrate Ansible automation into a CI/CD pipeline.

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| Ansible | Configuration Management & Automation |
| Jenkins | CI/CD Automation |
| Git & GitHub | Version Control |
| Linux (Ubuntu/Amazon Linux) | Target Servers |
| SSH | Secure Remote Connection |
| YAML | Playbook Definition |
| Bash | Installation Scripts |

---

# Repository Structure

```text
Ansible-Demo/
│
├── files/
│   └── Application files and configuration files
│
├── group_vars/
│   └── Variables shared across managed hosts
│
├── Jenkinsfile
│   └── Jenkins Pipeline
│
├── ansible.cfg
│   └── Ansible Configuration
│
├── ansible_install.sh
│   └── Script to install Ansible
│
├── ansible_playbook.yaml
│   └── Main Automation Playbook
│
└── README.md
```

---

# Workflow

1. Developer pushes code to GitHub.
2. Jenkins triggers the pipeline.
3. Jenkins executes the Ansible Playbook.
4. Ansible connects to remote servers over SSH.
5. Required packages are installed.
6. Configuration files are copied.
7. Services are started or restarted.
8. Deployment completes successfully.

---

# Prerequisites

Before running this project, ensure the following are installed:

- Linux Control Node
- Ansible
- Git
- SSH Key Pair
- Python 3
- Jenkins (Optional)
- Remote Linux Servers
- Internet Connectivity

---

# Deployment Steps

### Step 1

Clone the repository.

```bash
git clone https://github.com/<your-username>/Ansible-Demo.git
```

### Step 2

Install Ansible.

```bash
chmod +x ansible_install.sh
./ansible_install.sh
```

### Step 3

Verify installation.

```bash
ansible --version
```

### Step 4

Configure your inventory file.

Example:

```ini
[web]
172.31.xx.xx

[app]
172.31.yy.yy
```

### Step 5

Verify connectivity.

```bash
ansible all -m ping
```

### Step 6

Run the playbook.

```bash
ansible-playbook ansible_playbook.yaml
```

### Step 7

Verify that all tasks completed successfully.

---

# Skills Demonstrated

- Configuration Management
- Infrastructure Automation
- Infrastructure as Code (IaC)
- Linux Administration
- SSH Configuration
- YAML Playbook Development
- Ansible Roles and Variables
- CI/CD Integration
- Jenkins Pipeline Automation
- Git Version Control
- Server Provisioning
- Remote Configuration Management

---

# Future Improvements

- Implement Ansible Roles
- Use Ansible Vault for secrets management
- Integrate with AWS EC2 Dynamic Inventory
- Automate Docker installation
- Configure Kubernetes nodes
- Add Monitoring using Prometheus and Grafana
- Integrate with Terraform for complete Infrastructure Provisioning

---

# Author

**Seyi Akinmusere**

DevOps Engineer | Cloud Engineer

### Core Skills

- AWS Cloud
- Terraform
- Ansible
- Jenkins
- Docker
- Kubernetes
- Linux
- Git & GitHub
- CI/CD
- Infrastructure as Code
