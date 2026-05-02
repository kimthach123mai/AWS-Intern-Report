---
title: "Worklog tuần 3"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "

---
### Mục tiêu tuần 3
*	Triển khai và cấu hình EC2 để chạy ứng dụng web. 
*	Làm quen môi trường server Linux và lệnh cơ bản. 
*	Cài đặt và cấu hình web server (Apache) và PHP. 
*	Thiết lập kết nối ổn định giữa máy local và server cloud.

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Tạo EC2 instance (Amazon Linux 2)</li><li>Chọn instance phù hợp (t2.micro) </li><li>Tạo key pair để SSH</li><li>Cấu hình Security Group</li>|23/03/2026|23/03/2026|AWS Console|
|3|<ul style="margin:0"><li>SSH vào EC2 từ local</li><li>Thực hành lệnh Linux cơ bản</li><li>Update hệ thống</li>|24/03/2026|24/03/2026||
|4|<ul style="margin:0"><li>Cài Apache (httpd)</li><li>Bắt đầu và bật dịch vụ Apache</li><li>Kiểm tra bằng IP public</li></ul>|25/03/2026|25/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|5|<ul style="margin:0"><li>Cài PHP và extension</li><li>Cấu hình Apache chạy PHP</li><li>Tạo file test PHP (info.php)</li></ul>|26/03/2026|26/03/2026||
|6|<ul style="margin:0"><li>Test web server</li><li>Kiểm tra hiển thị web</li><li>Fix lỗi cơ bản</li></ul>|27/03/2026|27/03/2026||

### Kết quả đạt được
*	Triển khai thành công EC2 sử dụng Amazon Linux 2 với cấu hình đầy đủ. 
*	Cấu hình Security Group cho phép: 
  *	SSH (port 22) 
  *	HTTP (port 80) 
  *	HTTPS (port 443) 
*	Kết nối thành công từ máy local đến EC2 bằng SSH thông qua key pair. 
*	Làm quen môi trường Linux server: 
  *	Di chuyển thư mục 
  *	Quản lý quyền file 
  *	Sử dụng lệnh hệ thống 
*	Cài đặt và cấu hình Apache: 
  *	Bật service tự động chạy 
  *	Kiểm tra hoạt động qua IP public 
*	Cài đặt PHP và tích hợp với Apache: 
  *	Test file PHP thành công 
  *	Đảm bảo server xử lý được PHP 
*	Xác nhận môi trường server hoạt động ổn định: 
  *	Web server phản hồi tốt 
  *	Xử lý được các lỗi cơ bản 
*	Tạo nền tảng vững chắc cho việc deploy ứng dụng hoàn chỉnh ở các tuần tiếp theo.
