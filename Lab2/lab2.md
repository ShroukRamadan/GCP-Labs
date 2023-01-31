# GCP-Labs

## Lab#2

#### Lab 2.1

1. From Cloud console, create a VPC named “auto-vpc” with auto-mode enabled, How many subnets created?

![Screenshot from 2023-01-29 12-46-00](https://user-images.githubusercontent.com/57557314/215321026-17e219cb-4b35-491b-a193-2872e82b6306.png)

2. From Cloud console, create a VPC named “custom-vpc” with auto-mode disabled and create two subnets.


![Screenshot from 2023-01-29 12-46-23](https://user-images.githubusercontent.com/57557314/215321029-e5905c12-615a-4b43-a534-5aa9b2c9dddf.png)


3. Using gcloud tool list all available VPCs and list subnets of each VPC.

```
gcloud compute networks list
```

![Screenshot from 2023-01-29 11-50-08](https://user-images.githubusercontent.com/57557314/215321042-c04957e5-6094-4abd-99ac-50ffd6ca36d2.png)

```
gcloud compute networks subnets list --filter="network:custom-vpc"

```
![Screenshot from 2023-01-29 12-30-04](https://user-images.githubusercontent.com/57557314/215321067-cf3cf3de-2814-4dc3-8566-bfb47ef10127.png)



4. Block internet access from you VPC using firewall rules.

![Screenshot from 2023-01-29 12-47-48](https://user-images.githubusercontent.com/57557314/215321093-acfd1db1-50f3-4cc0-ab46-f578ce09a562.png)


5. Create a firewall rule to allow incoming SSH requests from internet to all instances in your vpc.

![Screenshot from 2023-01-29 12-48-48](https://user-images.githubusercontent.com/57557314/215321156-3baa96a8-666c-4179-8a5f-20dc762fd702.png)


6. Modify the previous firewall rule to allow only ssh requests coming through Google’s IAP servers.

![Screenshot from 2023-01-29 12-49-00](https://user-images.githubusercontent.com/57557314/215321160-ef261285-ea57-4c4c-96d3-02f5fd7ff651.png)
 

#### Lab 2.2


1. Create a VM with public ip then:
    - In two different ways, SSH into this VM.
     1. SSH From browser
       
     ![Screenshot from 2023-01-31 01-26-55](https://user-images.githubusercontent.com/57557314/215635987-96c61494-b950-4a1d-a865-d5f0051160a3.png)

     2. SSH using gcloud 
       
     ![Screenshot from 2023-01-31 01-10-34](https://user-images.githubusercontent.com/57557314/215636323-ccd2ef4f-61e7-4a31-9eb6-430626e021ea.png)

     

    - Enforce SSH into this VM to be IAP protected.
   
     ![Screenshot from 2023-01-31 01-29-08](https://user-images.githubusercontent.com/57557314/215633314-8eb5476f-8059-4cfa-bcc3-796ce419dd5f.png)

     ![Screenshot from 2023-01-31 03-08-46](https://user-images.githubusercontent.com/57557314/215633108-81486b01-c2d6-4ce3-a05f-45fb8b6842ec.png)


2. Create a VM without public ip then:
    - SSH into this vm.    
    - update system packages (is it possible?)
    
      ![Screenshot from 2023-01-31 01-38-35](https://user-images.githubusercontent.com/57557314/215633751-b5467db1-e8b5-4939-8dde-6d67c263b0b9.png)


3. Create a VM with public ip then:
    - SSH into this vm
    - Update system packages.
    
     ![Screenshot from 2023-01-31 03-17-41](https://user-images.githubusercontent.com/57557314/215634458-d301eb54-d215-4c95-9cd3-1392dd262579.png)

    - Setup Nginx Web Server and test your setup.
        
     ![Screenshot from 2023-01-31 03-34-04](https://user-images.githubusercontent.com/57557314/215636692-db1d174a-b7d5-4219-bb3f-21533ec6c0bd.png)

    - Create a custom image from this VM named “custom-img-nginx”.
    
     ![Screenshot from 2023-01-31 01-57-31](https://user-images.githubusercontent.com/57557314/215634666-5ed9e7c0-a16f-446d-a8a4-ec680a739763.png) 


4. Create MIG (min 3 and max 5) of a template using the custom image “custom-img-nginx”

 ![Screenshot from 2023-01-31 02-50-09](https://user-images.githubusercontent.com/57557314/215634822-b16d4656-7d6e-45f2-a2f6-7ba8627fad25.png)
 
 ![Screenshot from 2023-01-31 03-22-21](https://user-images.githubusercontent.com/57557314/215635082-18e41096-1623-4e37-b190-eed86e7baac4.png)

 ![Screenshot from 2023-01-31 02-30-02](https://user-images.githubusercontent.com/57557314/215635164-1c5e11f2-d711-4dc8-b5ea-9d96c78668cf.png)
