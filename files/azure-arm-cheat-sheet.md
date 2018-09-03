# Azure ARM Scripts Cheat Sheet

([Previous](../README.md))

- [Install azure cli on linux](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli-apt?view=azure-cli-latest)

- [Azure Quickstart Templates](https://github.com/Azure/azure-quickstart-templates)

--------

- `az group create --name <resource group name> --location "West Europe"` create a ressource group with specific location

- `az group deployment create --name <deployment name> --resource-group <resource group name> --template-file <template file>.json --parameters <parameters>` deploy a Json arm script with custom parameters on a specific resource group. 