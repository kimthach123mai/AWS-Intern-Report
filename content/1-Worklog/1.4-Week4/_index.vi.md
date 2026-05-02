---
title: "Worklog tuần 4"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---
### Mục tiêu tuần 4
*	Triển khai source code ứng dụng web lên EC2. 
*	Cấu hình Apache để host ứng dụng. 
*	Hiểu cấu trúc thư mục và phân quyền trên server Linux. 
*	Đảm bảo ứng dụng truy cập được qua IP public. 

### Công việc thực hiện trong tuần
|Thứ|Công việc|Ngày bắt đầu|Ngày hoàn thành|Nguồn tài liệu
|:-:|---|:-:|:-:|:-:|
|2|<ul style="margin:0"><li>Chuẩn bị source code trên máy local</li><li>Kiểm tra cấu trúc project</li><>Nén source code để upload</li>|30/03/2026|30/03/2026||
|3|<ul style="margin:0"><li>Upload source code lên EC2 bằng SCP/WinSCP </li><li>Kiểm tra file sau khi upload</li><li>Kiểm tra tính toàn vẹn của tệp sau khi chuyển.</li>|31/03/2026|31/03/2026|[AWS Docs](https://cloudjourney.awsstudygroup.com/)|
|4|<ul style="margin:0"><li>Copy source vào /var/www/html  </li><li>Cấu hình phân quyền file (chmod, chown) </li><li>Đảm bảo Apache truy cập được </li></ul>|01/04/2026|01/04/2026||
|5|<ul style="margin:0"><li>Cấu hình Apache (httpd.conf if needed)</li><li>Khởi động lại Apache service </li><li>Fix lỗi 403, permission</li></ul>|02/04/2026|02/04/2026||
|6|<ul style="margin:0"><li>Truy cập web qua IP public </li><li>Test giao diện và chức năng  </li><li>Fix lỗi hiển thị</li></ul>|03/04/2026|03/04/2026||

### Kết quả đạt được
* Triển khai thành công source code từ máy local lên EC2. 
* Upload file bằng SCP/WinSCP và kiểm tra dữ liệu sau khi upload. 
* Cấu hình cấu trúc thư mục trên server: 
  * Đặt source tại /var/www/html 
  * Sắp xếp file hợp lý 
* Quản lý phân quyền file hiệu quả: 
  * Sử dụng chmod, chown đúng cách 
  * Đảm bảo Apache có quyền truy cập 
* Cấu hình và restart Apache thành công: 
  * Fix lỗi _403 Forbidden, Permission denied_
  * Đảm bảo service hoạt động ổn định
* Deploy web thành công và truy cập qua IP public: 
  * Giao diện hiển thị đúng 
  * CSS, JS, hình ảnh load đầy đủ 
* Phát hiện và xử lý các lỗi phổ biến: 
  * Sai đường dẫn file 
  * Lỗi phân quyền 
  * Thiếu resource 
* Có kinh nghiệm thực tế trong việc deploy ứng dụng từ local lên cloud.