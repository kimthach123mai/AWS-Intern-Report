---
title: "Prerequisites"
date: 2026-05-01
weight: 1
chapter: false
pre: "<b> 4.3.1. </b>"
---

### Environment Requirements

Before initiating the deployment process for **Classic Groove**, the following technical prerequisites must be established to ensure a seamless integration of AWS services.

#### 1. Cloud Infrastructure Account
*   **AWS Management Console:** Access to an active AWS account is mandatory.
*   **Deployment Region:** The system is standardized on the **ap-southeast-2 (Sydney)** region to maintain consistency and service availability.

#### 2. Local Connectivity & Tools
*   **Terminal Interface:** Use of an SSH client (such as Git Bash or Terminal) for secure remote server management.
*   **Data Transfer:** Availability of Secure Copy Protocol (SCP) tools to migrate source code to the cloud environment.
*   **Dependency Management:** **Composer** must be installed to manage the AWS SDK for PHP, enabling EC2-to-S3 communication.

#### 3. Security & IAM Configuration
The deployment requires specific **IAM (Identity and Access Management)** permissions to manage resources according to the principle of least privilege:
*   Full access permissions for EC2, RDS, and S3 services.
*   Privileges to generate Access Keys for application-level authentication.