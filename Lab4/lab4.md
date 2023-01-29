# GCP-Labs

## Lab#4


1. Using gsutil:
    - Create 3 buckets.
    ```
    gsutil mb gs://<bucket-name>
    ```

    - Enable Versioning for them.
    ```
    gsutil versioning set on gs://<bucket-name>
    ```

    - Upload a file into bucket-1 then copy it from bucket-1 into bucket-2 & bucket-3.
    
    ```
    gsutil cp <local-file-path> gs://frist-bucket-123/
    ```
    
    ```
    gsutil cp gs:<file-path-in-bucket> gs://<bucket-name>/
    ```

    
    - Delete the file from bucket-1
    
    ```
    gsutil rm gs:<file-path-in-bucket>

    ```

2.Host a static website on a standard public GCS bucket [hint: link].

3.Deploy MySQL private instance and connect to it then create a new database 


