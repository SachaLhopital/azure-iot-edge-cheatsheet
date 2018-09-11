# Azure ARM Scripts Cheat Sheet

([Previous](../README.md))

- [Install azure cli on linux](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli-apt?view=azure-cli-latest)

- [Azure quickstart templates (from Github)](https://github.com/Azure/azure-quickstart-templates)

- [All ARM resources references/definitions](https://docs.microsoft.com/en-us/azure/templates/)

- [Setup parameters](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-templates-parameters)

--------

- `az group create --name <resource group name> --location "West Europe"` create a ressource group with specific location

- `az group deployment create --name <deployment name> --resource-group <resource group name> --template-file <template file>.json` deploy a Json arm script on a specific resource group. 

- `az group deployment validate --resource-group <resource group name> --template-file <template file>.json` validate whether a template is syntactically correct for specific user group.

- `az group deployment delete --name <deployment name> --resource-group <resource group name>` remove a specific deployment history from a resource group

- `az deployment create --name <deployment name> --template <template file>.json -l <location>` deploy resources *with no resource group associated* on a specific location. 

-------- 

#### Usefull Params :

- `--parameters <parameters>.json` to specify a custom `file.parameters.json` to auto setup the parameters of the script.

- `--mode {Complete, Incremental}` mode *Incremental* will add all resources to the resource group ; mode *Complete* will override **ALL** existing resources with the resources in the new arm script. 

- `--debug` for debug mode !
