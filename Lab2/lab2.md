# GCP-Labs

## Lab#2

#### Lab 2.1

1. From Cloud console, create a VPC named “auto-vpc” with auto-mode enabled, How many subnets created?


2. From Cloud console, create a VPC named “custom-vpc” with auto-mode disabled and create two subnets.




3. Using gcloud tool list all available VPCs and list subnets of each VPC.

```
gcloud compute networks list
```

```
gcloud compute networks subnets list --filter="network:custom-vpc"

```

4. Block internet access from you VPC using firewall rules.



5. Create a firewall rule to allow incoming SSH requests from internet to all instances in your vpc.


6. Modify the previous firewall rule to allow only ssh requests coming through Google’s IAP servers.



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