# AKS ARM Template
Deploys an AKS Cluster with supporting Infrastructure

## Instructions
- Review parameters in `azuredeploy.parameters.json`
- Edit accordingly. Review the Parameter Descriptions for more info on each
- Run Deployment with the following command:
```
az deployment group create --resource-group RESOURCEGROUP --template-file "azuredeploy.json" --parameters "azuredeploy.parameters.json"
```
Denote the need to specify a *RESOURCEGROUP*


*As a sidenote, you may wish to use the new --confirm-with-what-if feature to view changes.. This is still in previous, but can be invoked with..*
```
az deployment group create --confirm-with-what-if --resource-group RESOURCEGROUP --template-file "azuredeploy.json" --parameters "azuredeploy.parameters.json"
```

## Post-Deployment
Once deployed...
- Authenticate against the cluster:
```
az aks get-credentials --resource-group RESOURCEGROUP --name CLUSTERNAME
```
Denote the need to specify the *RESOURCEGROUP* and *CLUSTERNAME*