---
title : "Week 7 Worklog"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : "<b>1.7. </b>"
---
### Week 7 Objectives
* Integrate Amazon S3 into the web application for file storage. 
* Replace local file storage with cloud-based storage. 
* Understand S3 permissions, bucket policies, and access control. 
* Improve system scalability and storage efficiency. 

### Tasks to be carried out this week
|Day|Task|Start Date|Completion Date|Reference Material
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Create S3 bucket with appropriate naming convention</li><li>Configure region and storage settings</li><li>Disable block public access (for testing)</li></ul>|20/04/2026|20/04/2026|AWS Console|
|3|<ul style="margin:0"><li>Configure bucket policy and IAM permissions</li><li>Allow public read access for images</li><li>Test access via S3 URL</li></ul>|21/04/2026|21/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Integrate S3 into PHP application</li><li>Install AWS SDK for PHP</li><li>Configure credentials and region</li></ul>|22/04/2026|22/04/2026|AWS SDK Docs|
|5|<ul style="margin:0"><li>Implement file upload to S3</li><li>Retrieve and store S3 file URL in database</li><li>Modify application logic to use S3 URLs</li></ul>|23/04/2026|23/04/2026|PHP Docs|
|6|<ul style="margin:0"><li>Test file upload, display, and deletion</li><li>Debug upload errors (permission, size limit)</li><li>Optimize file handling performance</li></ul>|24/04/2026|24/04/2026||

### Acheievements
* Acquired comprehensive knowledge of Amazon S3, including bucket management, object storage, and access control mechanisms.
* Successfully performed S3 operations such as:
  * Uploading and downloading files 
  * Configuring public access 
  * Using S3 URLs to serve static content (images) 
* Understood Amazon RDS concepts: 
  * Database instance creation 
  * Endpoint usage for connection 
  * Automated backup and scaling capabilities 
* Compared cloud database (RDS) with traditional local MySQL: 
  * Recognized advantages in scalability and availability 
  * Understood managed service benefits 
* Successfully set up a local development environment: 
  * Installed Apache, MySQL, and PHP 
  * Built and tested database-driven web application locally 
* Gained basic knowledge of CloudWatch: 
  * Monitored system performance metrics 
  * Understood logging and alert mechanisms 
* Designed a basic cloud system architecture integrating: 
  * EC2 (Compute) 
  * RDS (Database) 
  * S3 (Storage)