# 🧠 Ansible Playbooks for AMD MI300x 8vm-sriov automation 
This repository provides a set of Ansible playbooks for orchestrating an AMD MI300X GPU environment using 8 virtual machines with SR-IOV, each VM assigned to a dedicated GPU. It automates the installation of ROCm and AMDGPU drivers FOR vm, sets up monitoring with amdgpu-exporter, performs health checks across all VMs & gpuS, and manages systemd services for continuous observability. 

## 🔧 Following playbooks are designed to:
- install_amdgpu_driver.yml - amdgpu driver installation across all 8VMs
- install_rocm_stack.yml - ROCm installation across all 8VMs
- install_amdgpu_exporter.yml - Exporter installation across 8VMs
- manage_exporter.yml - check and start exporter automatically across 8V
- check_amdgpu_status.yml - check and provide status of each GPU assigned to 8VMs
---

## ⚙️ Requirements

- MI300X GPUs with SR-IOV enabled
- 1 VF is assinged to each VM 
- Ansible 2.10+
- Passwordless SSH access to all VMs
- Inventory file (e.g., `inventory.ini`) with VM IPs and hostnames
- Ubuntu 22.04+ on all VMs
---
