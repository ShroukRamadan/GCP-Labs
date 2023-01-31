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
    - Enforce SSH into this VM to be IAP protected.


2. Create a VM without public ip then:
    - SSH into this vm.
    - update system packages (is it possible?)



3. Create a VM with public ip then:
    - SSH into this vm
    - Update system packages.
    - Setup Nginx Web Server and test your setup.
    - Create a custom image from this VM named “custom-img-nginx”.




4. Create MIG (min 3 and max 5) of a template using the custom image “custom-img-nginx”
