# GCP-Labs

#### Lab 3.1

1. In previous lab you created the VPC “auto-vpc”, How many routes created for this VPC? Can you delete any of these routes?

  the Number of routes is 36 , 35 local routes to the subnets within the VPC  and one route to the Internet via an Internet Gateway.

  I can't delete routes to the subnets but i can delete route to the Interne

  ![Screenshot from 2023-01-31 04-36-59](https://user-images.githubusercontent.com/57557314/215843283-b79a61ba-43c6-487b-9478-ed13f0618080.png)


2. In previous lab you created a VPC named “custom-vpc” How many routes created for this VPC?

  the Number of routes is 3

  ![Screenshot from 2023-01-31 04-36-21](https://user-images.githubusercontent.com/57557314/215843121-5a5a2abf-3b3b-437f-a217-8feda93b9c93.png)



3. How would you block internet access from you vpc using routes?

  by deleteing the defult route to the internet


4. Add a NAT gateway on any of the subnets in your VPC.


  ![Screenshot from 2023-01-31 13-49-23](https://user-images.githubusercontent.com/57557314/215843426-36be0bbd-51a7-49e3-aa37-47c0129fea1b.png)


#### Lab 3.2

1. In previous lab you created an MIG of a template using the custom image “custom-img-nginx”, Create a Global (or Regional) HTTP Load balancer to access your MIGs Nginx setup.



  ![Screenshot from 2023-01-31 05-51-19](https://user-images.githubusercontent.com/57557314/215843850-51335664-4109-4246-a945-52f2f202796c.png)


  ![Screenshot from 2023-01-31 05-51-24](https://user-images.githubusercontent.com/57557314/215843880-4c5c6e27-2028-4910-a58e-97aa99038136.png)


2. Try to configure IAP at the load balancer level to protect your ingress access. Is it possible to have IAP enabled for HTTP resources?

  I can't configure iIAP at my loadbalancer level as lb working in http protocol but IAP enabled in https  

  ![Screenshot from 2023-01-31 19-57-54](https://user-images.githubusercontent.com/57557314/215844100-ed9efc7d-34ae-42e2-80cd-3b2b8ef57a59.png)


#### Lab 3.3

1. Create a private standard GKE cluster.

  ![Screenshot from 2023-01-31 20-32-46](https://user-images.githubusercontent.com/57557314/215851039-41b8725f-fa86-4007-a985-9fe4875b1819.png)


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

  ![Screenshot from 2023-01-31 20-36-48](https://user-images.githubusercontent.com/57557314/215852041-ab0f54f4-8541-472b-968b-7854b6de0a3f.png)


  ![Screenshot from 2023-01-31 20-35-54](https://user-images.githubusercontent.com/57557314/215852057-9c626f51-92a2-47e7-b4ff-6cc78efcb407.png)



3. Expose your Nginx deployment using Kubernetes LoadBalancer Service.

  ```
  kubectl expose deployment nginx-deployment --port=80 --target-port=80 --name service-lb --type=LoadBalancer
  ```
  ```
  kubectl get svc
  ```
  ![Screenshot from 2023-01-31 20-39-31](https://user-images.githubusercontent.com/57557314/215852568-ad664f99-b6e3-4c95-8e2a-d71b7a202a4e.png)

  ![Screenshot from 2023-01-31 20-40-11](https://user-images.githubusercontent.com/57557314/215852652-c61c146e-5059-4884-9876-bec0b3916408.png)


4. What is the type of GCP Load Balancer that is created for your LB service?


![Screenshot from 2023-01-31 20-46-28](https://user-images.githubusercontent.com/57557314/215854688-59e7d9d8-042f-4263-bd57-1901cefe07d8.png)


5. Use kubectl to view container logs.

  ```
  kubectl get pods
  ```
  ```
  kubectl logs <pod-name>
  ```


  ![Screenshot from 2023-01-31 20-53-29](https://user-images.githubusercontent.com/57557314/215855456-ccd965b7-bacf-4379-a9ee-d1b540c95636.png)


6. Use cloud logging service to view container logs. 


  ![Screenshot from 2023-01-31 20-56-08](https://user-images.githubusercontent.com/57557314/215855990-dd909c9c-8f63-4473-8984-070a71aac6eb.png)


7. (Bonus) setup a HTTP load balancer for your deployment using the kubernetes ingress resource

  ![Screenshot from 2023-01-31 21-24-50](https://user-images.githubusercontent.com/57557314/215862249-7bd71683-3980-464e-a741-b48fefd770cb.png)

  ![Screenshot from 2023-01-31 21-24-44](https://user-images.githubusercontent.com/57557314/215862319-3e8fe169-0d37-4c8d-98c5-b69ffc556390.png)


8. Create an autopilot GKE cluster with public control plane.


  ![Screenshot from 2023-01-31 18-26-37](https://user-images.githubusercontent.com/57557314/215844998-0761ef77-da9a-4a25-a0ed-daac2e752a46.png)

9. Enforce the cluster’s control plane to accept only connections from your local machine

  ![Screenshot from 2023-01-31 20-01-08](https://user-images.githubusercontent.com/57557314/215844770-f3e421b1-43e6-48fb-92e9-233bf7ab5f68.png)

  ![Screenshot from 2023-01-31 19-01-06](https://user-images.githubusercontent.com/57557314/215844937-264130ba-ae14-49a2-9d87-edd9051bbde9.png) 
