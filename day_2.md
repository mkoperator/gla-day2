# Conduent Day 2 Training

## Questions and Comments from Yesterday?

## LAB: Hands on creating a Rancher cluster in AKS (aks_arm_cluster.md)
1. Create Namespace
2. Create Service Account
3. Give Service Account permissions
4. Use ARM template to deploy a 3 node cluster (scaling set can be used)

This gets us to a functional AKS cluster (not private)

## Rancher setup real lab
### Real way to do it with external load balancer
https://blog.kubernauts.io/aks-deployment-automation-with-terraform-and-multi-aks-cluster-management-with-rancher-6da9865ad52b
But this is simple way

1. Cert manager (conduent/day_2/aks-rancher/aks_cert_manager.md)
2. Nginx (conduent/day_2/aks-rancher/aks_nginx_ingress.md)
3. rancher (conduent/day_2/aks-rancher/aks_rancher_setup.md)
4. Correct Ingress Setting


##	Working with Rancher
2.2.1	WebUi Features
      - Projects
      - Resources
      - Monitoring
      - Logging
      - Security
      - Api
      
2.2.2	CLI
    - Example - List Projects
    https://rancher.com/docs/rancher/v2.x/en/cli/
    
2.2.3	API
    https://rancher.com/docs/rancher/v2.x/en/api/
    
2.2.4	Terraform
    https://www.terraform.io/docs/providers/rancher2/r/cluster.html
    

### 2.3	Deploying Clusters with Rancher
  2.3.1	AKS Example

  2.3.2	LAB: Add AKS Cluster via UI

  2.3.3	Importing Clusters
  
        Add separate cluster
        
  2.3.4	LAB: Import RKE Cluster

  2.4	RBAC /w Azure AD (rancher_configure_ad.md)
  
  2.4.2	Using Group Permissions

## LAB: Configure AD
### Create some groups and add yourself
1. Setup Service Account
2. Give Service Account permissions
3. Plug into rancher
