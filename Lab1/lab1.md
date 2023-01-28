# GCP-Labs

## Lab#1

#### Lab 1.1

1. Explore Google Cloud Console.

2. Setup a billing method on your google account.

3. Create a GCP project.

4. Assign your billing account to your project.

5. Setup project budget.

6. Setup billing alerts.

7. Using cloud shell, list all projects and set default project.

8. Install and configure gcloud SDK on your pc.

9. List all projects using gcloud SDK and set default project

#### Lab 1.2

1. From Cloud console, do the following:
    i. Create custom role named "my-custom-role-1" with the following permissions only:
        - Iam.roles.get
        - Iam.roles.list


2. From Cloud console, Explore primitive and pre-defined roles and their permissions.


3. From Cloud console, Create a service account with id "my-first-serviceaccount".


4. From Cloud console, Assign the custom role "my-custom-role-1" to the service account "my-first- serviceaccount"


5. Using gcloud,
    I. List all roles on your project.

    II. Describe the predefined role "roles/compute.viewer" and view its details & permissions

    III. Describe the custom role "my-custom-role-1" and view its details & permissions.
    
    IV. List all authenticated accounts.
    
    V. Activate the service account "my-first-serviceaccount".
    
    VI. List all authenticated accounts again.
    
    VII. Using this service account, try to list all roles on your project.
    
    VIII.Try to delete custom role "my-custom-role-1


