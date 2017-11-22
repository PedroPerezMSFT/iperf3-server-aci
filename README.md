# iperf3-server-aci
Azure ARM template to deploy an "iperf3 server" container, listening on 1 port (5201/TCP)

## Deployment
```
~ $ git clone https://github.com/PedroPerezMSFT/iperf3-server-aci
~ $ az group deployment create --resource-group netperftest --template-file .\iperf3-server-aci\azuredeploy.json
```
You can find the public IP address ACI has assigned your container from the output after running the above template:

    "outputs": {
      "containerIPv4Address": {
        "type": "String",
        "value": "1.2.3.4"
      }
    },
    
The above example shows 1.2.3.4 as your assigned public IP address.
