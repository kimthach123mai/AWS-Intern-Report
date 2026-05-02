---
title: "Week 3 Worklog"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
### Week 3 Objectives
*	Deploy and configure an EC2 instance for hosting the web application. 
*	Understand Linux server environment and basic command-line operations. 
*	Install and configure web server (Apache) and runtime environment (PHP). 
*	Establish a stable connection between local machine and cloud server.

### Tasks to be carried out this week
|Day|Task|Start Date|Completion Date|Reference Material
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Launch EC2 instance (Amazon Linux 2)</li><li>Select appropriate instance type (t2.micro) </li><li>Configure key pair for SSH access </li><li>Set up Security Group (open port 22, 80, 443) </li>|23/03/2026|23/03/2026|AWS Console|
|3|<ul style="margin:0"><li>Connect to EC2 via SSH using terminal</li><li>Practice basic Linux commands (ls, cd, chmod, sudo)</li><li>Update system packages </li>|24/03/2026|24/03/2026|Linux Docs|
|4|<ul style="margin:0"><li>Install Apache (httpd) web server </li><li>Start and enable Apache service </li><li>Verify installation via public IP</li></ul>|25/03/2026|25/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|5|<ul style="margin:0"><li>Install PHP and required extensions </li><li>Configure Apache to work with PHP  </li><li>Create test PHP file (info.php) </li></ul>|26/03/2026|26/03/2026||
|6|<ul style="margin:0"><li>Test web server environment </li><li>Verify HTTP response and page rendering </li><li>Troubleshoot common errors (permission, service issues) </li></ul>|27/03/2026|27/03/2026||

### Acheievements
*	Successfully deployed an EC2 instance using Amazon Linux 2 with proper configuration. 
*	Configured Security Group rules to allow: 
  *	SSH access (port 22) 
  *	HTTP access (port 80) 
  *	HTTPS access (port 443) 
*	Established a secure SSH connection from local machine to EC2 instance using key pair authentication. 
*	Gained hands-on experience with Linux server environment: 
  *	Navigating directories 
  *	Managing file permissions 
  *	Using administrative commands 
*	Installed and configured Apache web server: 
  *	Enabled service auto-start 
  *	Verified server availability via public IP 
*	Installed PHP and integrated with Apache: 
  *	Tested PHP execution using sample script 
  *	Ensured compatibility between Apache and PHP 
*	Verified that the server environment is fully operational: 
  *	Successfully served web pages 
  *	Handled basic troubleshooting scenarios 
*	Built a solid foundation for deploying a complete web application in the following weeks. 
