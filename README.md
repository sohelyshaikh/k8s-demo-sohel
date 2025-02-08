# k8s-demo-sohel


Steps to deploy this kubernetes application:
1. Configure AWS cli with propers access keys. 
2. Initiate terraform and apply the terraform configuration: Terraform will deploy the EKS cluster and it's managed nodegroup. 
3. Give access to your IAM user in EKS IAM Cluster Access tab. 
4. Update the Kube config file with aws eks update-kubeconfig command. 
5. Access the eks cluster and deploy the python application. 
6. Expose the python application with clusterIP. 
7. Install ingress controller and then create an ingress resource with rules. 
8. A load balancer will beb deployed and we can access the python application fromm this loadbalancer URL. 
9. Next deploy the prometheus for monitoring, first create config map with scraping config, then deploy prometheus application and then expose this via a NodePort service. 
10. Now prometheus UI can be accessed via nodeport url. 
