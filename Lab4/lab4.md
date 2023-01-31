# GCP-Labs

## Lab#4


1. Using gsutil:
    - Create 3 buckets.
    ```
    gsutil mb gs://<bucket-name>
    ```
   
   ![Screenshot from 2023-01-29 13-14-26](https://user-images.githubusercontent.com/57557314/215329707-16cac6bd-2fb1-4a3f-84b6-9d80b8432479.png)

   ![Screenshot from 2023-01-29 13-15-41](https://user-images.githubusercontent.com/57557314/215329777-81f131ed-23d6-4bd2-b3af-be07be7a1901.png)


    - Enable Versioning for them.
    ```
    gsutil versioning set on gs://<bucket-name>
    ```
    ![Screenshot from 2023-01-29 13-19-20](https://user-images.githubusercontent.com/57557314/215329825-cc99c7c1-22e0-4bd1-b45c-52642dd6a1d1.png)
    
    ![Screenshot from 2023-01-29 13-18-39](https://user-images.githubusercontent.com/57557314/215329850-bc7ee35c-9573-4799-b227-12d2ba58f6a6.png)


    - Upload a file into bucket-1 then copy it from bucket-1 into bucket-2 & bucket-3.
    
    ```
    gsutil cp <local-file-path> gs://frist-bucket-123/
    ```
       
    ![Screenshot from 2023-01-29 13-24-10](https://user-images.githubusercontent.com/57557314/215330150-81c2c634-0e27-40ef-9861-45443aa1ab1d.png)


    ![Screenshot from 2023-01-29 13-29-39](https://user-images.githubusercontent.com/57557314/215330157-6a41d482-e8e1-4cbc-aa86-91a61ddf8433.png)

    ```
    gsutil cp gs:<file-path-in-bucket> gs://<bucket-name>/
    ```
    
    ![Screenshot from 2023-01-29 13-28-13](https://user-images.githubusercontent.com/57557314/215329867-f2d69533-13b4-4547-8ac3-a4fb34288ccc.png)
    
    
    ![Screenshot from 2023-01-29 13-30-00](https://user-images.githubusercontent.com/57557314/215330001-0628a394-7eab-4bd3-8a4f-6942c7917b2e.png)

    ![Screenshot from 2023-01-29 13-30-17](https://user-images.githubusercontent.com/57557314/215330016-ea7b0bf3-079d-44f6-9640-d3481d304d24.png)

    - Delete the file from bucket-1
    
    ```
    gsutil rm gs:<file-path-in-bucket>

    ``` 
    ![Screenshot from 2023-01-29 13-32-32](https://user-images.githubusercontent.com/57557314/215330378-bd65bb50-b087-422b-9dd8-bf54d610e7f5.png)

     
    ![Screenshot from 2023-01-29 13-33-19](https://user-images.githubusercontent.com/57557314/215330410-af1ddbcd-0cf8-408e-a603-62a775e93933.png)


2.Host a static website on a standard public GCS bucket [hint: link].

![Screenshot from 2023-01-29 14-29-32](https://user-images.githubusercontent.com/57557314/215330497-057f7185-4528-4bc3-be89-a98c0a533752.png)


![Screenshot from 2023-01-29 14-30-18](https://user-images.githubusercontent.com/57557314/215330504-c87c920a-f0e3-4e57-94d2-a219a2f5e64c.png)


![Screenshot from 2023-01-29 14-29-09](https://user-images.githubusercontent.com/57557314/215330485-70b28e76-09cc-4e0d-a84d-f4a2a5c8b1df.png)



3.Deploy MySQL private instance and connect to it then create a new database 

![Screenshot from 2023-01-29 15-01-24](https://user-images.githubusercontent.com/57557314/215330549-4f6135fd-914b-49e6-8954-6792c30fe788.png)


![Screenshot from 2023-01-29 15-00-51](https://user-images.githubusercontent.com/57557314/215330537-63b1b23d-e853-4d49-b58f-3bc8318e2970.png)


#### Lab 4.2


1. Using gcloud & Docker:
    - Configure Docker & gcloud to work with GCR of your project. [hint: link]
    - Push Nginx docker image to GCR (make the image private).
    - Pull this image into a k8s setup or on a VM (hint: attach a SA on ur vm or gke with correct iam role).



2. Using Cloud Functions:
- Create a Function that runs whenever a file is uploaded to a cloud storage bucket. [hint: link]


3. Using Cloud Run:
- Run a pre-built docker image (pulled from GCR) [hint: link]
- Build and Run any sample app [hint: link]


4. Using App Engine:
- Run the sample hello-world python app [link]