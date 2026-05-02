---
title : "Worklog tuần 7"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : "<b>1.7. </b>"
---
### Mục tiêu tuần 7
* Tích hợp Amazon S3 vào ứng dụng web để lưu trữ file. 
* Thay thế lưu trữ local bằng lưu trữ trên cloud. 
* Hiểu về phân quyền S3 (bucket policy, access control). 
* Cải thiện khả năng mở rộng và lưu trữ của hệ thống. 

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Tạo S3 bucket</li><li>Cấu hình region và storage</li><li>Tắt block public access (test)</li></ul>|20/04/2026|20/04/2026|AWS Console|
|3|<ul style="margin:0"><li>Cấu hình bucket policy</li><li>Cho phép public read</li><li>Test truy cập URL</li></ul>|21/04/2026|21/04/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Tích hợp S3 vào code PHP</li><li>Cài AWS SDK</li><li>Cấu hình credentials</li></ul>|22/04/2026|22/04/2026|AWS SDK Docs|
|5|<ul style="margin:0"><li>Upload file lên S3</li><li>Lưu URL vào database</li><li>Sửa logic code</li></ul>|23/04/2026|23/04/2026|PHP Docs|
|6|<ul style="margin:0"><li>Test upload và hiển thị file</li><li>Fix lỗi upload</li><li>Tối ưu xử lý file</li></ul>|24/04/2026|24/04/2026||

### Kết quả đạt được
* Tạo và cấu hình thành công S3 bucket để lưu trữ file cho hệ thống. 
* Cấu hình phân quyền: 
  * Thiết lập bucket policy cho phép public read 
  * Quản lý quyền IAM 
  * Hiểu vấn đề bảo mật khi mở public access 
* Tích hợp S3 vào ứng dụng web: 
  * Cài đặt AWS SDK cho PHP 
  * Kết nối ứng dụng với S3 
* Xây dựng chức năng upload file: 
  * Upload file trực tiếp lên S3 
  * Lấy URL của file 
  * Lưu URL vào database 
* Cập nhật logic hệ thống: 
  * Thay thế lưu file local bằng S3 
  * Load hình ảnh từ S3 
* Test toàn bộ quy trình: 
  * Upload → Lưu URL → Hiển thị ảnh 
  * Đảm bảo file truy cập được 
* Phát hiện và xử lý lỗi: 
  * Lỗi permission do policy sai 
  * Giới hạn dung lượng file 
  * Lỗi định dạng file 
* Cải thiện kiến trúc hệ thống: 
  * Tách storage (S3) và server (EC2) 
  * Tăng khả năng mở rộng 
  * Giảm phụ thuộc vào server