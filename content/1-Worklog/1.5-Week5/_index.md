---
title : "Week 5 Worklog"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : "<b>1.5. </b>"
---
### Week 5 Objectives
* Deploy and configure Amazon RDS (MySQL) for cloud database usage. 
* Migrate database from local environment to RDS. 
* Establish connection between EC2 and RDS. 
* Integrate database into the web application and test CRUD operations. 

### Tasks to be carried out this week
|Day|Task|Start Date|Completion Date|Reference Material
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Create RDS MySQL instance</li><li>Configure instance type (db.t3.micro)</li><li>Set username, password, DB name</li><li>Enable public access (for testing)</li></ul>|06/04/2026|06/04/2026|AWS Console|
|3|<ul style="margin:0"><li>Configure Security Group for RDS</li><li>Open port 3306 for EC2 access</li><li>Whitelist EC2 security group</li><li>Retrieve RDS endpoint</li></ul>|07/04/2026|07/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Export database from local (mysqldump)</li><li>Import database into RDS</li><li>Verify tables and data</li></ul>|08/04/2026|08/04/2026|MySQL Docs|
|5|<ul style="margin:0"><li>Update application config (DB_HOST, DB_USER, DB_PASS)</li><li>Connect PHP application to RDS</li><li>Test connection and queries</li></ul>|09/04/2026|09/04/2026|PHP Docs|
|6|<ul style="margin:0"><li>Test full CRUD operations (Create, Read, Update, Delete)</li><li>Debug connection errors (timeout, access denied)</li><li>Optimize connection settings</li></ul>|10/04/2026|10/04/2026||

### Acheievements
* Successfully created and configured an Amazon RDS MySQL instance with appropriate settings for development and testing. 
* Configured networking and security properly: 
  * Opened port 3306 for database access 
  * Allowed EC2 instance to communicate with RDS via Security Group 
  * Understood how AWS isolates database services 
* Migrated database from local environment to cloud: 
  * Exported database using mysqldump 
  * Imported data into RDS without data loss 
  * Verified tables, relationships, and data integrity 
* Established successful connection between EC2 and RDS: 
  * Used RDS endpoint for remote connection 
  * Updated application configuration correctly 
* Integrated database into the web application: 
  * Connected PHP backend to RDS 
  * Executed SQL queries successfully 
* Verified full CRUD functionality: 
  * Create new records 
  * Retrieve and display data 
  * Update existing records 
  * Delete records 
* Identified and resolved common database connection issues: 
  * Connection timeout due to Security Group misconfiguration 
  * Access denied errors due to incorrect credentials 
  * Charset and encoding inconsistencies 
* Gained practical experience in deploying and managing cloud-based databases in a real-world scenario.