---
title: "Architecture & Design"
date: 2026-05-01
weight: 2
chapter: false
pre: "<b> 4.2. </b>"
---

### System Architecture

The **Classic Groove** infrastructure is built on a standard **3-Tier Architecture** to ensure the separation of concerns, scalability, and security. The design facilitates a clear data flow between the presentation, application, and data storage layers.



*   **Presentation & Application Layer:** Powered by **Amazon EC2** running a LAMP stack (Linux, Apache, MySQL client, PHP) to handle web requests and application logic.
*   **Database Layer:** Utilizes **Amazon RDS (MySQL)** for structured data management, including user accounts and vinyl record inventory.
*   **Storage Layer:** Employs **Amazon S3** for hosting static media assets and high-fidelity audio files.

![Architecture](/images/4.2-Architecture/architecture.png)

### Service Selection & Rationale

The selection of services is based on reliability, managed capabilities, and cost-efficiency:

*   **Amazon EC2 (t3.micro):** Chosen for its flexibility in environment configuration and eligibility for the AWS Free Tier, minimizing operational costs during the internship.
*   **Amazon RDS (MySQL):** Provides a managed database solution that automates backups and patching, ensuring data integrity for the e-commerce platform.
*   **Amazon S3:** Selected for its high durability and ability to serve large media files directly via public URLs, reducing the load on the web server.

### Security & Compliance

*   **Network Security:** Security Groups act as virtual firewalls to control inbound and outbound traffic. Only essential ports (80 for HTTP, 443 for HTTPS, and 22 for SSH) are open.
*   **Access Management:** IAM Roles and Policies are configured following the principle of **Least Privilege**, ensuring services only have the permissions necessary for their specific tasks.
*   **Data Protection:** No sensitive credentials or Access Keys are hard-coded within the source code.