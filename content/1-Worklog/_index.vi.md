---
title: "Nhật ký công việc"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1. </b> "
---


Trong trang này, tôi trình bày worklog (nhật ký công việc) của dự án Classic Groove theo từng tuần và từng ngày.

Worklog giúp theo dõi tiến độ thực hiện, các nhiệm vụ đã hoàn thành, cũng như những vấn đề gặp phải trong quá trình triển khai hệ thống.

Dự án được thực hiện trong vòng 8 tuần (2 tháng), với mục tiêu xây dựng và triển khai một ứng dụng web hoàn chỉnh trên nền tảng cloud (AWS).

**Tuần 1:** [Tìm hiểu AWS và các dịch vụ EC2, RDS. Tạo tài khoản AWS và cấu hình IAM theo nguyên tắc least privilege.](1.1-week1/)

**Tuần 2:** [Phân tích yêu cầu và thiết lập môi trường local (LAMP). Xây dựng và test database MySQL.](1.2-week2/)

**Tuần 3:** [Tạo EC2 (Amazon Linux 2), cấu hình Security Group (22, 80, 443), tạo key SSH. Cài Apache và PHP.](1.3-week3/)

**Tuần 4:** [Upload source bằng SCP và deploy vào /var/www/html. Cấp quyền file và kiểm tra web. ](1.4-week4/)

**Tuần 5:** [Tạo RDS MySQL, mở port 3306, cấu hình Security Group. Kết nối EC2 với RDS và import database. ](1.5-week5/)

**Tuần 6:** [Xử lý lỗi kết nối MySQL 8 và charset. Cài php-mysqlnd, nâng cấp PHP. Tạo file testdb.php để kiểm tra kết nối.](1.6-week6/)

**Tuần 7:** [Cấu hình kết nối database trong code (dataProvider.php) bằng mysqli_real_connect (SSL). Restart Apache và test hệ thống. ](1.7-week7/)

**Tuần 8:** [ Kiểm thử hệ thống, debug lỗi và kiểm tra chức năng. Viết tài liệu và hoàn thiện báo cáo. ](1.8-week8/)
