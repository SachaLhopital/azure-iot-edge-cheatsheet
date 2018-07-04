# Azure IoT Edge Cheat Sheet

([Previous](../README.md))

- [Install azure cli on linux](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli-apt?view=azure-cli-latest)

- `pip3 install azure-iot-edge-runtime-ctl` install using python 3

-------------

- `az iot hub create --resource-group <ressource_group_name> --name <iot_hub_name> --sku F1` create an iot hub for a specific ressource group using a specific princing tier *F1*

- `az iot hub device-identity create --device-id <device_id> --hub-name <iot_hub_name> --edge-enabled` create edge device in the iot hub

-------------

- `iotedgectl setup --connection-string "<connection_string> --auto-cert-gen-force-no-password"` setup the iot edge runtime on the target machine (with no password). 

- `iotedgectl login --address <container_registry_name>.azurecr.io --username <container_registry_name> --password <password>` login to the iot edge runtime

- `iotedgectl start` start the iot edge runtime (and all modules)

- `iotedgectl stop` stop the iot edge runtime (and all modules)