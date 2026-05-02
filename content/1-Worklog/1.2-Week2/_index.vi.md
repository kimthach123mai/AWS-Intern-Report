---
title: "Worklog tuần 2"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2
*	Tìm hiểu chuyên sâu về dịch vụ lưu trữ và cơ sở dữ liệu trên AWS (S3, RDS). 
*	Nắm cách giám sát hệ thống bằng CloudWatch. 
*	Thiết lập môi trường phát triển local để test ứng dụng. 
*	Chuẩn bị cấu trúc ứng dụng trước khi deploy lên cloud.

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Tìm hiểu S3: bucket, object, storage class</li><li>Tạo và quản lý bucket</li><li>Học cách phân quyền truy cập</li>|16/03/2026|16/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|3|<ul style="margin:0"><li>Thực hành upload/download file S3</li><li>Cấu hình public access</li><li>Test hiển thị ảnh từ S3</li>|17/03/2026|17/03/2026|AWS Console|
|4|<ul style="margin:0"><li>Tìm hiểu RDS: instance, endpoint </li><li>So sánh với MySQL local </li><li>Học backup và scaling</li></ul>|18/03/2026|18/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|5|<ul style="margin:0"><li>Cài đặt môi trường local (Apache, MySQL, PHP) </li><li>Tạo database và dữ liệu mẫu  </li><li>Test kết nối DB bằng PHP </li></ul>|19/03/2026|19/03/2026||
|6|<ul style="margin:0"><li>Tìm hiểu CloudWatch </li><li>Theo dõi tài nguyên EC2  </li><li>Xem log và alarm</li><li>Vẽ sơ đồ kiến trúc hệ thống (EC2 + RDS + S3) </li></ul>|20/03/2026|20/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|

### Kết quả đạt được
* Nắm vững dịch vụ Amazon S3: 
  *	Quản lý bucket và object 
  * Hiểu cơ chế phân quyền truy cập 
* Thực hành thành công các thao tác với S3:  
  *	Upload và download file 
  *	Cấu hình public access
  * Hiển thị ảnh thông qua URL S3 
* Hiểu rõ dịch vụ Amazon RDS: 
  *	Tạo database instance  
  *	Kết nối thông qua endpoint  
  *	Backup tự động và khả năng mở rộng 
* So sánh được RDS với MySQL local:  
  *	Nhận thấy ưu điểm về scalability và availability  
  *	Hiểu lợi ích của managed service  
* Thiết lập thành công môi trường local:  
  *	Cài Apache, MySQL, PHP 
  *	Xây dựng và test ứng dụng web 
* Có kiến thức cơ bản về CloudWatch:  
  *	Theo dõi hiệu năng hệ thống  
  *	Hiểu log và cảnh báo 
* Thiết kế được sơ đồ kiến trúc hệ thống: 
  *	EC2 (Compute) 
  *	RDS (Database) 
  *	S3 (Storage) 
