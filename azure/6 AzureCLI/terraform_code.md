## Define the provider
```sh
provider  "azurerm"{

//Configuration for Authentictaion with Azure Cloud

 subscription_id = "9e80acc3-ca87-4e6b-85fd-8f3ddf0e1172"
 tenant_id = "22770cf1-4936-4b74-9d98-fd4d7e10f346"
 client_id = "bda553f2-36e4-470e-a552-a7b296e9a7b2"
 client_secret = "*************************"

 features {
    resource_group {
       prevent_deletion_if_contains_resources = false
     }
}
   
}
```
## Define the Resource group
```sh
resource "azurerm_resource_group" "example" {
  name     = "RSG4"
  location = "West Europe"
}
```
## Define the virtual network
```sh
resource "azurerm_virtual_network" "example" {
  name                = "terraform-vnet"
  location            = azurerm_resource_group.example.location
  resource_group_name = azurerm_resource_group.example.name
  address_space       = ["10.0.0.0/16"]
}
```
## Define the subnet
```sh
resource "azurerm_subnet" "internal" {
  name                 = "terraform-subnet"
  resource_group_name  = azurerm_resource_group.example.name
  virtual_network_name = azurerm_virtual_network.example.name
  address_prefixes     = ["10.0.2.0/24"]
}
```
## Define the interface
```sh
resource "azurerm_network_interface" "main" {
  name                = "terraform-nic"
  location            = azurerm_resource_group.example.location
  resource_group_name = azurerm_resource_group.example.name

  ip_configuration {
    name                          = "testconfiguration1"
    subnet_id                     = azurerm_subnet.internal.id
    private_ip_address_allocation = "Dynamic"
  }
}
```
## Define the virtual machine
```sh
resource "azurerm_virtual_machine" "main" {
  name                  = "terraform-vm"
  location              = azurerm_resource_group.example.location
  resource_group_name   = azurerm_resource_group.example.name
  network_interface_ids = [azurerm_network_interface.main.id]
  vm_size               = "Standard_DS1_v2"

  storage_image_reference {
    publisher = "Canonical"
    offer     = "0001-com-ubuntu-server-jammy"
    sku       = "22_04-lts"
    version   = "latest"
  }
  storage_os_disk {
    name              = "myosdisk1"
    caching           = "ReadWrite"
    create_option     = "FromImage"
    managed_disk_type = "Standard_LRS"
  }
  os_profile {
    computer_name  = "hostname"
    admin_username = "testadmin"
    admin_password = "Password1234!"
  }
  os_profile_linux_config {
    disable_password_authentication = false
  }
 tags = {
    environment = "staging"
  }
}
```
