# NGINX Ingress Controller
## Add repository
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx

## add Namespace
kubectl create ns ingress-nginx

## switch to nginx Namespace
kubens ingress-nginx

## install NGINX
helm install nginx-ingress stable/nginx-ingress \
    --namespace ingress-nginx \
    --set controller.replicaCount=2 \
    --set controller.nodeSelector."beta\.kubernetes\.io/os"=linux \
    --set defaultBackend.nodeSelector."beta\.kubernetes\.io/os"=linux

# get external ip address
kubectl get all


# give external ip to mikhail to get your own sub domain @simpleblocks.net
