# Azure aks steps

## installation steps
Resourec group creation

az group create --name myResourceGroup --location eastus

cluster creation

az aks create -g myResourceGroup -n myAKSCluster --enable-managed-identity --node-count 2 --enable-addons monitoring --enable-msi-auth-for-monitoring  --generate-ssh-keys

az aks install-cli

az aks get-credentials --resource-group myResourceGroup --name myAKSCluster

kubectl get nodes

# delete resource group 

az group delete --name myResourceGroup --yes --no-wait