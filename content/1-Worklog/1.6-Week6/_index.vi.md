---
title : "Worklog tuần 6"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : "<b>1.6. </b>"
---
### Mục tiêu tuần 6
* Phát hiện và xử lý lỗi giữa EC2–RDS và ứng dụng web. 
* Tối ưu hiệu năng hệ thống và truy vấn database. 
* Cải thiện độ ổn định của hệ thống. 
* Tích lũy kinh nghiệm debug hệ thống thực tế trên cloud. 

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Phân tích lỗi kết nối EC2–RDS</li><li>Kiểm tra Security Group</li><li>Xác nhận endpoint, port, tài khoản</li></ul>|13/04/2026|13/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|3|<ul style="margin:0"><li>Fix lỗi kết nối DB</li><li>Sửa config PHP</li><li>Bật debug</li></ul>|14/04/2026|14/04/2026|PHP Docs|
|4|<ul style="margin:0"><li>Fix lỗi encoding</li><li>Sửa lỗi hiển thị dữ liệu</li><li>Đồng bộ DB và app</li></ul>|15/04/2026|15/04/2026|MySQL Docs|
|5|<ul style="margin:0"><li>Tối ưu query SQL</li><li>Test tốc độ truy vấn</li><li>Cải thiện index</li></ul>|16/04/2026|16/04/2026||
|6|<ul style="margin:0"><li>Test toàn hệ thống</li><li>Tìm lỗi còn lại</li><li>Ghi lại cách xử lý</li></ul>|17/04/2026|17/04/2026||

### Kết quả đạt được
* Phát hiện và xử lý thành công nhiều lỗi thực tế trong hệ thống, đặc biệt là kết nối EC2–RDS. 
* Fix các lỗi quan trọng liên quan database: 
  * Lỗi timeout do Security Group cấu hình sai 
  * Lỗi “Access Denied” do sai tài khoản hoặc quyền 
  * Đảm bảo kết nối ổn định giữa web và database 
* Nâng cao kỹ năng debug: 
  * Bật hiển thị lỗi trong PHP 
  * Sử dụng log để xác định nguyên nhân lỗi 
  * Áp dụng quy trình debug có hệ thống 
* Xử lý lỗi encoding: 
  * Chuẩn hóa UTF-8 giữa DB và ứng dụng 
  * Fix lỗi hiển thị tiếng Việt 
  * Đảm bảo dữ liệu hiển thị đúng 
* Tối ưu hiệu năng database: 
  * Viết lại query chưa tối ưu 
  * Giảm truy vấn dư thừa 
  * Cải thiện tốc độ xử lý 
* Cải thiện độ ổn định hệ thống: 
  * Loại bỏ lỗi runtime 
  * Hệ thống hoạt động mượt hơn 
* Test toàn bộ hệ thống: 
  * Kiểm tra giao diện, backend và database 
  * Đảm bảo chức năng hoạt động đúng 
* Ghi lại các lỗi và cách xử lý: 
  * Tạo tài liệu tham khảo cho việc phát triển sau này