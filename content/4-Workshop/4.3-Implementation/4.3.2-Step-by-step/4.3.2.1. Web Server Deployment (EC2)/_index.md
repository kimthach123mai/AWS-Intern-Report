---
title: "Web Server Deployment"
weight: 1
pre: "<b> 4.3.2.1. </b>"
---

### Objective
Create a virtual server on AWS to host the PHP application logic for the **Classic Groove** store.

### Execution Steps

#### 1. Instance Initialization
*   **Service:** Access the **EC2 Dashboard** and select **Launch Instance**.
*   **Instance Name:** `classic-groove-server`.
*   **Operating System:** Select **Amazon Linux 2023** (or Amazon Linux 2).
*   **Instance Type:** `t3.micro` (Free Tier eligible).

#### 2. Access Security
*   **Key Pair:** Generate a new key pair named `aws-key.pem`.
*   **Security Group:** Create a new group allowing the following inbound traffic:
    *   **SSH (Port 22):** Limited to specific administrative IP.
    *   **HTTP (Port 80):** Open to the internet for web access.
    *   **HTTPS (Port 443):** Open for secure web access.

#### 3. Finalization
*   Confirm storage settings (Default 8GB) and click **Launch Instance**.
*   Record the **Public IPv4 Address** for future connectivity.