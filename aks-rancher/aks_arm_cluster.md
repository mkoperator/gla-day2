# Use our three node cluster ARM template to create the cluster.
az deployment group create --name rpso-rancher --resource-group conduent --template-file template.json --parameters parameters.json

## Runtime ~ 10

# Get credentials
az aks get-credentials --resource-group conduent --name rpso-rancher
