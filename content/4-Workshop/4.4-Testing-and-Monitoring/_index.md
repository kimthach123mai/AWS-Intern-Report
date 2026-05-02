---
title: "Testing & Monitoring"
date: 2026-05-01
weight: 4
chapter: false
pre: "<b> 4.4. </b>"
---

### System Validation

After deploying the cloud infrastructure, a series of comprehensive tests are conducted to ensure that the **Classic Groove** application operates seamlessly across all AWS tiers.

#### 1. End-to-End Functional Testing
*   **Web Accessibility:** Verified that the store is reachable via the Elastic IP and Public DNS on standard web ports.
*   **Media Streaming:** Confirmed that high-fidelity audio previews are served directly from Amazon S3 without latency or permission errors.
*   **Transaction Logic:** Tested the CRUD operations (Create, Read, Update, Delete) for the vinyl inventory and shopping cart, ensuring data persistence in Amazon RDS.

#### 2. Security & Connectivity Audit
*   **Database Isolation:** Confirmed that the RDS instance is not directly accessible from the public internet, requiring the EC2 web server as an intermediary.
*   **IAM Verification:** Validated that the EC2 instance utilizes assigned roles to communicate with S3, eliminating the need for hardcoded credentials.

#### 3. Operational Monitoring
*   **Resource Utilization:** Monitored CPU and memory usage of the `t3.micro` instance to ensure stability during peak simulated traffic.
*   **Billing Oversight:** Regularly reviewed the AWS Billing Dashboard to verify that costs remain within the estimated budget of approximately **$5.81/month**.

---

> **Conclusion:** The testing phase confirms that the integration between compute, database, and storage layers is successful, providing a stable environment for the digital music marketplace.