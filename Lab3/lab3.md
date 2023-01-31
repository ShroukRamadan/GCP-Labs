# GCP-Labs

#### Lab 3.1

1. In previous lab you created the VPC “auto-vpc”, How many routes created for this VPC? Can you delete any of these routes?

the Number of routes is 36 , 35 local routes to the subnets within the VPC  and one route to the Internet via an Internet Gateway.

yes, i can delete any of these routes




2. In previous lab you created a VPC named “custom-vpc” How many routes created for this VPC?

the Number of routes is 3



3. How would you block internet access from you vpc using routes?

by deleteing the defult route to the internet



4. Add a NAT gateway on any of the subnets in your VPC.



#### Lab 3.2
1. In previous lab you created an MIG of a template using the custom image “custom-img-nginx”, Create a Global (or Regional) HTTP Load balancer to access your MIGs Nginx setup.





2. Try to configure IAP at the load balancer level to protect your ingress access. Is it possible to have IAP enabled for HTTP resources?

I can't configure iIAP at my loadbalancer level as lb working in http protocol but IAP enabled in https  



#### Lab 3.3

1. Create a private standard GKE cluster.




2. Deploy Nginx as a deployment using latest Nginx docker image on Docker Hub.

```
sudo apt-get install google-cloud-sdk-gke-gcloud-auth-plugin 
```
```
gcloud container clusters get-credentials cluster-1 --zone us-central1-c --project shrouk-iti
```
```
kubectl create deployment nginx-deployment --image=nginx:latest
```
```
kubectl get deployments
```



3. Expose your Nginx deployment using Kubernetes LoadBalancer Service.

```
kubectl expose deployment nginx-deployment --port=80 --target-port=80 --name service-lb --type=LoadBalancer
```
```
kubectl get services
```

4. What is the type of GCP Load Balancer that is created for your LB service?



5. Use kubectl to view container logs.

```
kubectl get pods
```

```
kubectl logs <pod-name>
```


6. Use cloud logging service to view container logs. [hint: search about cloud logging service for gke]




7. (Bonus) setup a HTTP load balancer for your deployment using the kubernetes ingress resource




8. Create an autopilot GKE cluster with public control plane.




9. Enforce the cluster’s control plane to accept only connections from your local machine


