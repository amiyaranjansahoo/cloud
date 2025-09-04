
<img width="746" height="329" alt="image" src="https://github.com/user-attachments/assets/da5a56fb-9212-469b-b104-314120e7bcf2" />


## Azure CLI: 
```sh
AZURE CLI stands for "Azure Command Line Interface"
It is a command line utility for the Azure cloud in the local machine to create the infrastructure
To use the azure cli commands in the local machine,we should download & install the Azure CLI tool/software
```

## Installation Azure CLI in the windows machine:
```sh
Google ------------> search for "Azure CLI download for windows"
                                      |
                           open the official Microsoft website link
                                      |
                          Then select the "MSI file for Azure CLI" to download
                                      |
                           After downloading,then click on the setup file to install
After installation of Azure CLI in the local windows machine,then use the following command to check the
version of installed Azure CLI tool
                                    az --version
```
## Azure CLI Authentication
```sh
We can install azure cli in Azure Cloud Shell, local laptop or in a Azure VM. 
After the Azure CLI is installed, then authenticate using the below command

                                az login
                           az login --tenant <tennant id>
By using the above command will open the UI window/prompt to enter the azure subscription credentials to login
After login we can use the azure cli commands to create the resources like vnet,subnets,vm's,Application gateways etc...
```
# Azure cli Documents Ref
```sh
https://learn.microsoft.com/en-us/cli/azure/reference-docs-index?view=azure-cli-latest
Install => Installation reference
conceptual articles => CLI Reference
```

## Azure cli command to create vnet & subnets in azure account:
```sh
syntax:

az network vnet create \
  --resource-group <resource-group-name> \
  --name <vnet-name> \
  --address-prefix <vnet-address-prefix> \
  --location <location>
```
## Example:
```sh
az network vnet create \
  --resource-group myResourceGroup \
  --name myVnet \
  --address-prefix 10.0.0.0/16 \
  --location eastus # --location SouthCentralUS
```
## Create Subnets inside the VNet:
You can create multiple subnets by running az network vnet subnet create command for each subnet.
```sh
syntax:
az network vnet subnet create \
  --resource-group <resource-group-name> \
  --vnet-name <vnet-name> \
  --name <subnet-name> \
  --address-prefix <subnet-address-prefix>
```
## Example
```sh
az network vnet subnet create \
  --resource-group myResourceGroup \
  --vnet-name myVnet \
  --name subnet1 \
  --address-prefix 10.0.1.0/24

az network vnet subnet create \
  --resource-group myResourceGroup \
  --vnet-name myVnet \
  --name subnet2 \
  --address-prefix 10.0.2.0/24
```
## azure cli command to create the virtual machine
```sh
syntax:
az vm create \
  --resource-group <ResourceGroupName> \
  --name <VMName> \
  --image <ImageName> \
  --admin-username <AdminUsername> \
  --admin-password <AdminPassword>
```
## Explanation:
```sh
--resource-group: The name of the resource group where the VM will be created (must already exist).
--name: The name you want to assign to the VM.
--image: The OS image to use, like UbuntuLTS, Win2019Datacenter, etc.
--admin-username: The admin username for the VM.
--admin-password: The admin password for the VM (for Linux, you can also use --ssh-key-value to provide an SSH key instead).
Example:
az vm create \
  --resource-group MyResourceGroup \
  --name MyVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --ssh-key-value ~/.ssh/id_rsa.pub
```sh
