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




