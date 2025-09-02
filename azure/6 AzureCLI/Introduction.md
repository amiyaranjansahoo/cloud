
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
After the Azure CLI installed in the locam machine,then to use azure cli commands to create resource/infrastructure
in the Azure cloud,we should authenticate with the azure cloud from the local machine by using the following azure
cli command

                                az login

By using the above command will open the UI window/prompt to enter the azure subscription credentials to login
After login we can use the azure cli commands to create the resources like vnet,subnets,vm's,Application gateways etc...
```
