---
title: "Worklog"
date: 2026/04/27
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

This page presents the work log for the Classic Groove project, broken down by week and day.

The work log helps track progress, completed tasks, and any issues that need to be addressed during the development of the declaration system.

The project will be completed within 8 weeks (2 months), with the goal of building and developing a complete web application on a cloud-based operating system (AWS).

**Week 1:** [Studied AWS fundamentals and core services (EC2, RDS). Created AWS account and configured IAM user with least privilege.](1.1-week1/)

**Week 2:** [Analyzed project requirements and prepared local development environment using LAMP stack. Built and tested MySQL database locally. ](1.2-week2/)

**Week 3:** [Provisioned EC2 instance (Amazon Linux 2), configured Security Group (SSH, HTTP, HTTPS), and created SSH key pair. Installed Apache and PHP. ](1.3-week3/)

**Week 4:** [Uploaded project source code using SCP and deployed to Apache web root (/var/www/html). Configured file permissions and tested application via public IP. ](1.4-week4/)

**Week 5:** [Created Amazon RDS (MySQL) instance, configured Security Group for database access, and enabled public access. Connected EC2 to RDS and imported database using SQL dump.](1.5-week5/)

**Week 6:** [Troubleshot database connection issues, including MySQL 8 compatibility and charset errors. Installed php-mysqlnd and upgraded PHP version. Created test script (testdb.php) to validate EC2–RDS connection.](1.6-week6/)

**Week 7:** [Configured database connection in application source (dataProvider.php) using mysqli_real_connect with SSL. Restarted Apache and validated full system functionality. ](1.7-week7/)

**Week 8:** [Performed system testing and debugging. Verified all application features and database operations. Documented deployment process and prepared final report.](1.8-week8/)

