# Create a VM

Learn how to create an AlmaLinux Virtual Machine (VM) in Azure.

---

## Create

<img src="./assets_vm_create/01._Create.png" alt="use Free services"/>

<img src="./assets_vm_create/02._Create.png" alt="choose Linux VM"/>

<img src="./assets_vm_create/03._Create.png" alt="create a resource group"/>

<img src="./assets_vm_create/04._Create.png" alt="give name choose regions Almalinux"/>

<img src="./assets_vm_create/05._Create.png" alt="add ssh key review + create"/>

<img src="./assets_vm_create/06._Create.png" alt="validate create"/>

<img src="./assets_vm_create/07._Create.png" alt="wait until creation"/>

<img src="./assets_vm_create/08._Create.png" alt="go to resource"/>

<img src="./assets_vm_create/09._Create.png" alt="vm overview ip address"/>

---

## Assigning a public IP Address to the VM

<img src="./assets_vm_connect/01._vm_network_port.png" alt="go to the network interface"/>

<img src="./assets_vm_connect/02._change_ip_configuration.png" alt="change the ip configuration"/>

<img src="./assets_vm_connect/03._select_ip_address.png" alt="select the ip address"/>

<img src="./assets_vm_connect/04._create_public_ip_address.png" alt="create a public ip address"/>

<img src="./assets_vm_connect/05._SSH.png" alt="ssh into the vm"/>

---

## Delete

Once finished, remember to delete the resource group. Azure will still charge for the resources even if you don't use them. Even with a deleted VM, other resources like storage accounts and network interfaces will still be charged. 

**IMPORTANT**: Always delete the resource group if you are done with a VM.

<img src="./assets_vm_delete/01._Delete.png" alt="go to resource group"/>

<img src="./assets_vm_delete/02._Delete.png" alt="select and delete resource group"/>

<img src="./assets_vm_delete/03._Delete.png" alt="confirm delete"/>

<img src="./assets_vm_delete/04._Delete.png" alt="wait to confirm deletion"/>