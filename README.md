# Nexus Deployment Project

## Overview

This project demonstrates **automated deployment of Nexus Repository Manager** on AWS using **Ansible, Packer, and Terraform**.

It includes:

- Nexus installation with Ansible  
- AMI creation with Packer  
- Infrastructure provisioning with Terraform  
- Full automation workflow  

---

## Repository Structure

```text
nexus-deployment/
├─ NexusProject/
│  ├─ step2-ansible/          # Ansible playbooks to install Nexus
│  ├─ step3-packer/           # Packer configuration to build AMI
│  ├─ step4-terraform/        # Terraform scripts
│  ├─ step5-module/           # Terraform modules
├─ terraform-nexus-workflow/  # Terraform workflow project
├─ docs/
│  └─ nexus-workflow.png      # Deployment workflow diagram
├─ README.md




---

## Deployment Diagram

<p align="center">
  <img src="docs/nexus-workflow.png" alt="Deployment Workflow" width="600">
</p>

---

## Deployment Steps

1️⃣ **Clone Repository**

```bash
git clone https://github.com/bayanur5/nexus-deployment.git
cd nexus-deployment


2️⃣ Install Nexus with Ansible

cd NexusProject/step2-ansible
ansible-playbook -i inventory install_nexus.yml



3️⃣ Build Nexus AMI with Packer

cd ../step3-packer
packer build nexus.pkr.hcl

4️⃣ Provision Infrastructure with Terraform

cd ../../terraform-nexus-workflow
terraform init
terraform plan
terraform apply


5️⃣ Access Nexus

URL: http://<EC2_PUBLIC_IP>:8081
Admin password: /opt/sonatype-work/nexus3/admin.password


Author
GitHub: bayanur5

Technologies Used
AWS EC2
Terraform
Packer
Ansible
Nexus Repository Manager
