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

![Screenshot from 2023-02-01 23-53-09](https://user-images.githubusercontent.com/57557314/216372277-1c724277-b18e-4816-968c-c902c50cb2ce.png)

###### I can't connect to private Sql Instance so I create Public VM To connect to MySQL Instance


![Screenshot from 2023-02-02 17-48-54](https://user-images.githubusercontent.com/57557314/216372868-ff43e7b5-d010-45b5-aadb-610e839105e0.png)


#### Lab 4.2


1. Using gcloud & Docker:
    - Configure Docker & gcloud to work with GCR of your project. [hint: link]
        
        ```
        gcloud auth configure-docker
        ```
        
        ![Screenshot from 2023-02-02 18-42-17](https://user-images.githubusercontent.com/57557314/216386974-f34dc6db-aa7b-458f-9967-0603a93badc2.png)
       
    - Push Nginx docker image to GCR (make the image private).
    
    ```
     docker tag my-nginx gcr.io/shrouk-iti/my-nginx

    ```
    
    ```
     # gcloud docker -- push gcr.io/[PROJECT_ID]/[iMG-NAME] --make-private
     gcloud docker -- push gcr.io/shrouk-iti/my-nginx --make-private
    ```
    
    ![Screenshot from 2023-02-02 18-39-29](https://user-images.githubusercontent.com/57557314/216387152-67f26b7f-33b4-441f-ba74-87a63fefe891.png)
    
    
    ![Screenshot from 2023-02-02 18-41-29](https://user-images.githubusercontent.com/57557314/216387260-805edc26-5973-4a22-b7ed-af28153f4ce5.png)


    - Pull this image into a k8s setup or on a VM (hint: attach a SA on ur vm or gke with correct iam role).
    
     ###### Create a Service Account (docker-sa) with permission Storage Object Viewer role.
    
      ![Screenshot from 2023-02-02 18-53-51](https://user-images.githubusercontent.com/57557314/216390471-9ca1ad1c-2ea9-4ac1-87ba-d03722a2788c.png)
     
     
     
     
     #####  Create cluster
     
    
    ![Screenshot from 2023-02-02 20-00-11](https://user-images.githubusercontent.com/57557314/216405198-deedf147-e97a-43a9-94ae-6481a7693425.png)

    ###### Deploy inginx app using image in google container registery
    
    ![Screenshot from 2023-02-02 19-59-18](https://user-images.githubusercontent.com/57557314/216405780-ebf8236e-1b96-427a-90b8-025e812899ed.png)

    


2. Using Cloud Functions:
   - Create a Function that runs whenever a file is uploaded to a cloud storage bucket. [hint: link]
     
     ![Screenshot from 2023-02-02 20-39-59](https://user-images.githubusercontent.com/57557314/216419604-39ebb8bf-4248-45a8-b778-dd8774727969.png)
     
     ![Screenshot from 2023-02-02 20-26-57](https://user-images.githubusercontent.com/57557314/216419304-78e7c7f9-baea-48b7-8095-8c60f29472dc.png)


3. Using Cloud Run:
   - Run a pre-built docker image (pulled from GCR) [hint: link]
      
   
   
   - Build and Run any sample app [hint: link]


4. Using App Engine:
   - Run the sample hello-world python app [link]
