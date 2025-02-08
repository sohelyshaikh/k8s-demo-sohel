# k8s-demo-sohel


Steps to deploy this kubernetes application:
1. Configure AWS cli with propers access keys.
2. Build the docker image and push it to ECR. 
3. Initiate terraform and apply the terraform configuration: Terraform will deploy the EKS cluster and it's managed nodegroup. 
4. Give access to your IAM user in EKS IAM Cluster Access tab. 
5. Update the Kube config file with aws eks update-kubeconfig command. 
6. Access the eks cluster and deploy the python application. 
7. Expose the python application with clusterIP. 
8. Install ingress controller and then create an ingress resource with rules. 
9. A load balancer will beb deployed and we can access the python application fromm this loadbalancer URL. 
10. Next deploy the prometheus for monitoring, first create config map with scraping config, then deploy prometheus application and then expose this via a NodePort service. 
11. Now prometheus UI can be accessed via nodeport url. 
