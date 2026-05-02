---
title : "Worklog tuần 5"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : "<b>1.5. </b>"
---
### Mục tiêu tuần 5
* Triển khai và cấu hình Amazon RDS (MySQL). 
* Chuyển database từ local lên RDS. 
* Kết nối EC2 với RDS. 
* Tích hợp database vào web và test CRUD. 

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Tạo RDS MySQL</li><li>Cấu hình instance</li><li>Thiết lập user, password</li><li>Bật public access</li></ul>|06/04/2026|06/04/2026|AWS Console|
|3|<ul style="margin:0"><li>Cấu hình Security Group RDS</li><li>Mở port 3306</li><li>Cho phép EC2 truy cập</li><li>Lấy endpoint</li></ul>|07/04/2026|07/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Export DB local</li><li>Import vào RDS</li><li>Kiểm tra dữ liệu</li></ul>|08/04/2026|08/04/2026|MySQL Docs|
|5|<ul style="margin:0"><li>Sửa config database (DB_HOST, DB_USER, DB_PASS)</li><li>Kết nối PHP với RDS</li><li>Test query</li></ul>|09/04/2026|09/04/2026|PHP Docs|
|6|<ul style="margin:0"><li>Test CRUD</li><li>Fix lỗi kết nối DB</li><li>Tối ưu kết nối</li></ul>|10/04/2026|10/04/2026||

### Kết quả đạt được
* Tạo và cấu hình thành công Amazon RDS MySQL với cấu hình phù hợp cho môi trường test. 
* Cấu hình networking và bảo mật: 
  * Mở port 3306 để truy cập database 
  * Cho phép EC2 kết nối với RDS thông qua Security Group 
  * Hiểu cách AWS cô lập database 
* Chuyển database từ local lên cloud: 
  * Export bằng mysqldump 
  * Import lên RDS thành công 
  * Kiểm tra dữ liệu đầy đủ, không lỗi 
* Kết nối thành công EC2 với RDS: 
  * Sử dụng endpoint của RDS 
  * Cập nhật config ứng dụng đúng 
* Tích hợp database vào ứng dụng web: 
  * Kết nối PHP với RDS 
  * Thực thi query thành công 
* Test đầy đủ chức năng CRUD: 
  * Thêm dữ liệu (Create) 
  * Lấy dữ liệu (Read) 
  * Cập nhật (Update) 
  * Xóa (Delete) 
* Phát hiện và xử lý các lỗi phổ biến: 
  * Lỗi timeout do Security Group 
  * Sai user/password 
  * Lỗi encoding/charset 
* Có kinh nghiệm thực tế trong việc triển khai database trên cloud và tích hợp vào hệ thống. 