---
title : "Week 6 Worklog"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : "<b>1.6. </b>"
---
### Week 6 Objectives
* Identify and fix issues related to EC2–RDS connection and web application errors. 
* Optimize system performance and database queries. 
* Improve system stability and reliability. 
* Gain hands-on experience in debugging real-world cloud systems. 

### Tasks to be carried out this week
|Day|Task|Start Date|Completion Date|Reference Material
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Analyze connection issues between EC2 and RDS</li><li>Check Security Group configuration</li><li>Verify endpoint, port, and credentials</li></ul>|13/04/2026|13/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|3|<ul style="margin:0"><li>Fix database connection errors (timeout, access denied)</li><li>Adjust DB config in PHP</li><li>Enable error reporting for debugging</li></ul>|14/04/2026|14/04/2026|PHP Docs|
|4|<ul style="margin:0"><li>Resolve charset and encoding issues (UTF-8)</li><li>Fix data display errors on UI</li><li>Ensure compatibility between DB and application</li></ul>|15/04/2026|15/04/2026|MySQL Docs|
|5|<ul style="margin:0"><li>Optimize SQL queries (reduce redundancy, improve performance)</li><li>Test response time of queries</li><li>Improve database indexing if needed</li></ul>|16/04/2026|16/04/2026||
|6|<ul style="margin:0"><li>Perform full system testing (UI + backend + DB)</li><li>Identify remaining bugs</li><li>Document issues and solutions</li></ul>|17/04/2026|17/04/2026||

### Acheievements
* Successfully identified and resolved multiple real-world issues in the system, especially related to EC2–RDS connectivity. 
* Fixed critical database connection problems: 
  * Resolved timeout issues caused by incorrect Security Group configuration 
  * Fixed “Access Denied” errors due to incorrect credentials or permissions 
  * Ensured stable connection between application and database 
* Improved debugging skills: 
  * Enabled detailed error reporting in PHP 
  * Used logs and error messages to trace issues effectively 
  * Applied systematic debugging approach 
* Resolved character encoding issues: 
  * Standardized UTF-8 encoding across database and application 
  * Fixed incorrect display of Vietnamese characters 
  * Ensured consistent data handling 
* Optimized database performance: 
  * Refactored inefficient SQL queries 
  * Reduced redundant queries 
  * Improved response time for data retrieval 
* Enhanced system stability: 
  * Eliminated major runtime errors 
  * Improved reliability under normal usage 
* Conducted full system testing: 
  * Verified UI, backend logic, and database operations 
  * Ensured all features function correctly 
* Documented common issues and solutions, creating a valuable reference for future development and troubleshooting. 