# Install Cert Manager
https://cert-manager.io/docs/installation/kubernetes/

## Install with helm (CRDs)
kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v0.14.3/cert-manager.crds.yaml

## Install Jet Pack stack
helm repo add jetstack https://charts.jetstack.io

## Update Repo
helm repo update

## Create Namespace
kubectl create namespace cert-manager

# Helm v3+
helm install cert-manager jetstack/cert-manager  --namespace cert-manager --version v0.14.3

## Validate Installation
kubectl get pods --namespace cert-manager

### if you have to re-install rnacher, you have to remove and re-add cert Manager
