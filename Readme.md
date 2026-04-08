Prerequicites
----------
https://azure.microsoft.com/free/   -->login
https://developer.hashicorp.com/terraform/downloads -->download terraform
terraform -version
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli -->download az CLI
az version
----------
using azure cli account login and setup
az login
az account set --subscription "your-subscription-id"  --set subscription
---
Step-by-Step Terraform VM Creation
mkdir terraform-azure-vm
cd terraform-azure-vm
vim provider.tf
vim main.tf
terraform init
terraform validate
terraform plan
terraform apply
-----
Note----
VM size and image must use the same Hypervisor Generation
if 
size = "Standard_FX2ms_v2"
hypervisor
source_image_reference {
  publisher = "Canonical"
  offer     = "0001-com-ubuntu-server-jammy"
  sku       = "22_04-lts-gen2"
  version   = "latest"
}
