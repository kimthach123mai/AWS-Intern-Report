---
title: "Environment & Application Setup"
weight: 2
pre: "<b> 4.3.2.2. </b>"
---

### Connection & Updates
Securely connect to the instance via SSH using the downloaded key:
```bash
chmod 400 aws-key.pem
ssh -i "aws-key.pem" ec2-user@<your-public-ip>
sudo dnf update -y
```

### Connection & Updates
Deploy the necessary web server components:
Apache Web Server: sudo dnf install httpd -y
PHP Environment: sudo dnf install php php-mysqlnd -y
Service Activation:
```bash
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Source Code Deployment
Upload: Transfer the Classic Groove source code from the local machine using SCP:
```bash
scp -i aws-key.pem -r Classic-Groove-main ec2-user@<public-ip>:/home/ec2-user/
```
Web Root Configuration: Move files to the Apache document root and adjust permissions:
```bash
sudo cp -r ~/Classic-Groove-main/* /var/www/html/
sudo chmod -R 777 /var/www/html
```
Verification: Access http://<public-ip> to ensure the application is reachable.
