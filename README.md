
# Azure Execution Environment (EE) from Minimal EE

This repository contains a custom Ansible Execution Environment (EE) built from Red Hat's minimal EE image. It includes the `azure.azcollection` for automating Microsoft Azure infrastructure.

---

## 📌 Example Use Case: Provision Azure Resources

This EE can be used to automate common Azure tasks such as:

- Creating virtual machines
- Managing resource groups
- Deploying Azure networking components

### Example Playbook Task

```yaml
- name: Create a resource group in Azure
  hosts: localhost
  connection: local
  tasks:
    - name: Create resource group
      azure.azcollection.azure_rm_resourcegroup:
        name: myResourceGroup
        location: eastus
