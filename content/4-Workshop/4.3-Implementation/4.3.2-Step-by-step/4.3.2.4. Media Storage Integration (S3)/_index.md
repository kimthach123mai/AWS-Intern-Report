---
title: "Media Storage Integration (S3)"
weight: 4
pre: "<b> 4.3.2.4. </b>"
---

### Objective
Offload static assets and high-fidelity audio files from the web server to **Amazon S3** to improve application performance and scalability.

### Execution Steps

#### 1. S3 Bucket Creation
*   **Service:** Access the **S3 Dashboard** and select **Create bucket**.
*   **Bucket Name:** `classic-groove-media-assets` (Must be globally unique).
*   **Region:** Select **ap-southeast-2 (Sydney)** to match the EC2 instance.
*   **Object Ownership:** Enable **ACLs enabled** to manage individual file permissions.
*   **Block Public Access:** Uncheck "Block all public access" to allow public viewing of media assets.

#### 2. Identity and Access Management (IAM)
To allow the EC2 instance to upload files to S3 securely:
*   **Create IAM User:** Create a user named `classic-groove-s3-admin`.
*   **Attach Policy:** Assign the `AmazonS3FullAccess` policy.
*   **Security Credentials:** Generate and save the **Access Key ID** and **Secret Access Key**.

#### 3. Application Integration
*   **SDK Installation:** Use **Composer** on the EC2 instance to install the AWS SDK for PHP:
    ```bash
    composer require aws/aws-sdk-php
    ```
*   **Code Configuration:** Update the application's storage logic to utilize the S3 client:
    ```php
    $s3Client = new Aws\S3\S3Client([
        'region'  => 'ap-southeast-2',
        'version' => 'latest',
        'credentials' => [
            'key'    => 'YOUR_ACCESS_KEY',
            'secret' => 'YOUR_SECRET_KEY',
        ],
    ]);
    ```

#### 4. Data Migration
*   Upload existing vinyl album covers and audio previews from the local environment to the S3 bucket using the AWS Console or AWS CLI.
*   Update database records in RDS to point to the new S3 object URLs.