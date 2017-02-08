# Azure Container Registry - Frequently Asked Questions

## Can I create Azure Container Registry using ARM Template?
Yes. Here is the template that you can use to create a registry - https://github.com/Azure/azure-cli/blob/master/src/command_modules/azure-cli-acr/azure/cli/command_modules/acr/template.json

## Is there security vulnerability scanning for images in ACR?

Yes. Please check the following links

Twistlock - https://www.twistlock.com/2016/11/07/twistlock-supports-azure-container-registry/

Aqua - http://blog.aquasec.com/image-vulnerability-scanning-in-azure-container-registry


## How to configure Kubernetes with Azure Container Registry?
http://kubernetes.io/docs/user-guide/images/#using-azure-container-registry-acr


## How to access Docker Registry HTTP API V2?
ACR supports Docker Registry HTTP API V2. The APIs can be accessed at
https://\<your registry login server\>/v2/

## Is Azure Premium Storage account supported?
Azure Premium Storage account is not supported.

## How to get admin login credential for a container registry?

Please make sure admin is enabled.

Using `az cli`
```
az acr credential show -n myRegistry
```

Using `Azure Powershell`
```
Invoke-AzureRmResourceAction -Action getCredentials -ResourceType Microsoft.ContainerRegistry/registries -ResourceGroupName myResourceGroup -ResourceName myRegistry
```