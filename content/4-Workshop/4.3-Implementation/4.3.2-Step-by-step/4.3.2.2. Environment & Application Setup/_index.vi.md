---
title: "Thiết lập môi trường và Ứng dụng"
weight: 2
pre: "<b> 4.3.2.2. </b>"
---

### Kết nối và Cập nhật
Kết nối an toàn vào máy chủ qua SSH bằng khóa đã tải về:
```bash
chmod 400 aws-key.pem
ssh -i "aws-key.pem" ec2-user@<your-public-ip>
sudo dnf update -y
```

### Cài đặt phần mềm (LAMP Stack)
Triển khai các thành phần máy chủ web cần thiết[cite: 1]:
Máy chủ Apache: sudo dnf install httpd -y
Môi trường PHP: sudo dnf install php php-mysqlnd -y
Kích hoạt dịch vụ:
```bash
sudo systemctl start httpd
sudo systemctl enable httpd
```

### Triển khai mã nguồn
Tải lên: Chuyển mã nguồn dự án Classic Groove từ máy cục bộ bằng SCP:
```bash
scp -i aws-key.pem -r Classic-Groove-main ec2-user@<public-ip>:/home/ec2-user/
```
Cấu hình thư mục Web: Di chuyển tệp tin vào thư mục gốc của Apache và điều chỉnh quyền truy cập:
```bash
sudo cp -r ~/Classic-Groove-main/* /var/www/html/
sudo chmod -R 777 /var/www/html
```
Xác minh: Truy cập http://<public-ip> để đảm bảo ứng dụng đã hoạt động trên môi trường web.
