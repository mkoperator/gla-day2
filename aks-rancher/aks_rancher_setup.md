# add helm repo
helm repo add rancher-latest https://releases.rancher.com/server-charts/latest

# Add namespace
kubectl create ns cattle-system

# Install Rancher
helm install rancher rancher-latest/rancher \
  --namespace cattle-system \
  --set auditLog.level=1

## Validate Installation
kubectl -n cattle-system rollout status deploy/rancher

# copy down the ingress
kubectl get ingress -o yaml > ingress.yaml

# add nginx annotation to rancher Ingress
kubernetes.io/ingress.class: "nginx"
