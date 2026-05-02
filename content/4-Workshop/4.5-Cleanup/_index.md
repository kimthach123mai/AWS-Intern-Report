---
title: "Optimization & Clean-up"
date: 2026-05-01
weight: 5
chapter: false
pre: "<b> 4.5. </b>"
---

### Optimization Strategies

The **Classic Groove** project is optimized to balance operational performance with cost-efficiency, ensuring professional-grade delivery on a student budget.

*   **Cost Efficiency:** Utilization of `t3.micro` and `db.t3.micro` instances ensures the infrastructure remains within the AWS Free Tier limits wherever possible.
*   **Performance Tuning:** Media assets are served directly from Amazon S3, reducing the processing overhead on the EC2 web server and improving page load times for high-fidelity audio previews.
*   **Security Best Practices:** Access is restricted through Security Groups, allowing only necessary traffic on ports 80, 443, and 22. IAM policies follow the principle of least privilege to safeguard cloud resources.

---

### Resource Clean-up Procedure

To prevent unexpected charges after the project concludes, a systematic decommissioning of resources is performed:

1.  **Database Termination:** Delete the Amazon RDS instance `classic-groove-db`. Note: Ensure "Create final snapshot" is unchecked unless a backup is specifically required.
2.  **Compute Decommissioning:** Terminate the Amazon EC2 instance `classic-groove-server`. This action automatically releases the associated EBS volumes.
3.  **Storage Removal:** Empty and delete the Amazon S3 bucket `classic-groove-media-assets`. All vinyl album art and audio files must be removed before the bucket can be deleted.
4.  **Network & Security:** Remove custom Security Groups and release any allocated Elastic IP addresses to avoid idle resource fees.

> **Final Note:** Following this clean-up protocol ensures the AWS account returns to a zero-cost state while maintaining a clean environment for future projects.