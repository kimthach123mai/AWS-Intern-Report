---
title: "Week 4 Worklog"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "

---
### Week 4 Objectives
*	Deploy the web application source code to the EC2 server. 
*	Configure Apache web server to host the application properly. 
*	Understand file structure and permission management on Linux server. 
*	Ensure the application can be accessed via public IP.

### Tasks to be carried out this week
|Day|Task|Start Date|Completion Date|Reference Material
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Prepare application source code on local machine </li><li>Review project structure (HTML, CSS, PHP, assets) </li><li>Compress source code for transfer </li>|30/03/2026|30/03/2026||
|3|<ul style="margin:0"><li>Transfer source code to EC2 using SCP/WinSCP </li><li>Upload files to home directory</li><li>Verify file integrity after transfer </li>|31/03/2026|31/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Move source code to Apache root directory (/var/www/html) </li><li>Configure file permissions (chmod, chown) </li><li>Ensure Apache can read/write files </li></ul>|01/04/2026|01/04/2026||
|5|<ul style="margin:0"><li>Configure Apache (httpd.conf if needed)</li><li>Restart Apache service </li><li>Fix common issues (403 Forbidden, permission denied)</li></ul>|02/04/2026|02/04/2026||
|6|<ul style="margin:0"><li>Access application via EC2 Public IP </li><li>Test UI, routing, and page loading </li><li>Debug display errors and missing resources </li></ul>|03/04/2026|03/04/2026||

### Acheievements
* Successfully deployed the web application source code from local machine to EC2 server. 
* Transferred files securely using SCP/WinSCP and verified data integrity after upload. 
* Configured the correct file structure on the server: 
  * Placed application files in /var/www/html
  * Organized assets, scripts, and resources properly 
* Managed file permissions effectively:
  * Applied appropriate chmod and chown settings 
  * Ensured Apache had necessary access rights 
* Configured and restarted Apache server successfully: 
  * Resolved common errors such as _403 Forbidden and Permission Denied_
  * Verified that Apache service runs continuously 
* Deployed a working web application accessible via Public IP: 
  * Verified UI rendering 
  * Ensured static resources (CSS, JS, images) load correctly 
* Identified and fixed common deployment issues: 
  * Broken file paths 
  * Incorrect permissions 
  * Missing dependencies 
* Gained practical experience in real-world deployment process from local to cloud environment. 
