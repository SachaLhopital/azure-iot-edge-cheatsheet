# Azure IoT Edge Cheat Sheet

([Previous](../README.md))

- [Install azure cli on linux](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli-apt?view=azure-cli-latest)

- `az iot hub create --resource-group <ressource_group_name> --name <iot_hub_name> --sku F1` create an iot hub for a specific ressource group using a specific princing tier *F1*

- `az iot hub device-identity create --device-id <device_id> --hub-name <iot_hub_name> --edge-enabled` create edge device in the iot hub

-------------

## V1

- `pip3 install azure-iot-edge-runtime-ctl` install using python 3

- `iotedgectl setup --connection-string "<connection_string> --auto-cert-gen-force-no-password"` setup the iot edge runtime on the target machine (with no password). 

- `iotedgectl login --address <container_registry_name>.azurecr.io --username <container_registry_name> --password <password>` login to the iot edge runtime

- `iotedgectl start` start the iot edge runtime (and all modules)

- `iotedgectl stop` stop the iot edge runtime (and all modules)

-------------

## V2

- [Install IoT Edge on linux](https://docs.microsoft.com/en-us/azure/iot-edge/quickstart-linux)  

- `sudo nano /etc/iotedge/config.yaml` configuration file for iot edge runtime

- **/!\\** the connection between the iot edge runtime and the container registry must be setup with the portal (on the *Set Modules* page). **/!\\** 

- `sudo systemctl start iotedge` start the iot edge runtime (and all modules)

- `sudo systemctl restart iotedge` restart the iot edge runtime (and all modules)

- `sudo systemctl stop iotedge` stop the iot edge runtime (and all modules)

- `sudo systemctl status iotedge` gives the current status of the iot edge runtime

- `journalctl -u iotedge` retrieve the service logs

- `sudo iotedge list` view the modules running on  the device

- `sudo iotedge logs <module name> -f` view the logs of a specific module

