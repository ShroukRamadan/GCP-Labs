# GCP-Labs

## Lab#1

#### Lab 1.1

1. Explore Google Cloud Console.

![Screenshot from 2023-01-28 22-05-00](https://user-images.githubusercontent.com/57557314/215296193-255816ad-22a5-4b2e-b223-f7beaafb77f5.png)

2. Setup a billing method on your google account.

![Screenshot from 2023-01-28 22-08-27](https://user-images.githubusercontent.com/57557314/215296230-e6907491-68f0-46a9-b14d-642fb36e3892.png)

3. Create a GCP project.

![Screenshot from 2023-01-28 22-14-35](https://user-images.githubusercontent.com/57557314/215296273-8c894a6b-63a0-4387-8385-86dd0d6d1577.png)

4. Assign your billing account to your project.

![Screenshot from 2023-01-28 22-20-56](https://user-images.githubusercontent.com/57557314/215296288-bba01b91-cffd-4dda-863b-79f66dd4e192.png)


5. Setup project budget.

![Screenshot from 2023-01-28 22-28-09](https://user-images.githubusercontent.com/57557314/215296310-0ad21519-8d79-4bee-a4d0-43dd8d76ea02.png)

6. Setup billing alerts.

![Screenshot from 2023-01-28 22-28-09](https://user-images.githubusercontent.com/57557314/215296310-0ad21519-8d79-4bee-a4d0-43dd8d76ea02.png)

7. Using cloud shell, list all projects and set default project.

![Screenshot from 2023-01-28 22-31-34](https://user-images.githubusercontent.com/57557314/215296357-59981d2c-5d24-40f6-8e1a-09a9e2e0fdcd.png)

![Screenshot from 2023-01-28 22-33-36](https://user-images.githubusercontent.com/57557314/215296384-860674b2-437f-40ed-b7d4-98e4f2ba7886.png)

8. Install and configure gcloud SDK on your pc.

![Screenshot from 2023-01-29 01-56-08](https://user-images.githubusercontent.com/57557314/215296538-5ab08d4f-8712-4c18-8e99-e43fc19740f7.png)


9. List all projects using gcloud SDK and set default project

![Screenshot from 2023-01-28 23-38-32](https://user-images.githubusercontent.com/57557314/215296566-a0ad4831-e9be-4c20-b79f-1c00c2b73a7d.png)


#### Lab 1.2

1. From Cloud console, do the following:
    1. Create custom role named "my-custom-role-1" with the following permissions only:
        - Iam.roles.get
        - Iam.roles.list

![Screenshot from 2023-01-29 02-00-13](https://user-images.githubusercontent.com/57557314/215296653-8df57dbe-0fa7-4dcc-8969-512779ad1701.png)

2. From Cloud console, Explore primitive and pre-defined roles and their permissions.


3. From Cloud console, Create a service account with id "my-first-serviceaccount".

![Screenshot from 2023-01-29 02-02-41](https://user-images.githubusercontent.com/57557314/215296711-220b6c8a-9ca7-4dcd-a6e7-ca7d59520218.png)

4. From Cloud console, Assign the custom role "my-custom-role-1" to the service account "my-first- serviceaccount"


![Screenshot from 2023-01-29 02-04-06](https://user-images.githubusercontent.com/57557314/215296749-13bb0d9d-4c47-4940-a292-abd91989e7e4.png)

5. Using gcloud,
    1. List all roles on your project.
    
    ![Screenshot from 2023-01-29 02-05-36](https://user-images.githubusercontent.com/57557314/215296780-64b12c2a-dea6-4b79-a09a-bcfe10dd0cc9.png)


    2. Describe the predefined role "roles/compute.viewer" and view its details & permissions
    
    ![Screenshot from 2023-01-29 02-06-13](https://user-images.githubusercontent.com/57557314/215296799-764f8ebe-b576-40a1-b913-67329e5c74f4.png)
    

    3. Describe the custom role "my-custom-role-1" and view its details & permissions.
    
    
    ![Screenshot from 2023-01-29 01-07-46](https://user-images.githubusercontent.com/57557314/215296867-1af430bb-c231-4c07-bab8-f08609838f0b.png)

    
    4. List all authenticated accounts.
    
    ![Screenshot from 2023-01-29 01-10-10](https://user-images.githubusercontent.com/57557314/215296882-f56674e8-7687-4686-9bbc-f7e9f8dda1d7.png)

    5. Activate the service account "my-first-serviceaccount".
    
    ![Screenshot from 2023-01-29 01-19-08](https://user-images.githubusercontent.com/57557314/215296921-5235bd00-d2c3-4e7a-bd5c-db909beac763.png)
    
    6. List all authenticated accounts again.
    
    ![Screenshot from 2023-01-29 01-20-10](https://user-images.githubusercontent.com/57557314/215297549-f22712c7-d0dc-4d41-90ba-2d08be07c94f.png)

    7. Using this service account, try to list all roles on your project.
    
    ![Screenshot from 2023-01-29 01-23-52](https://user-images.githubusercontent.com/57557314/215297208-0e528a90-1855-4bcd-a37b-5270dff78fb7.png)
    

    8.Try to delete custom role "my-custom-role-1

    ![Screenshot from 2023-01-29 01-26-09](https://user-images.githubusercontent.com/57557314/215296987-d1da45cd-2e5b-40d9-9239-509f1d240845.png)
