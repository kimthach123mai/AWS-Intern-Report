---
title: "Kiến trúc và Thiết kế"
date: 2026-05-01
weight: 2
chapter: false
pre: "<b> 4.2. </b>"
---

### Kiến trúc hệ thống

Hạ tầng của dự án **Classic Groove** được xây dựng dựa trên mô hình **Kiến trúc 3 lớp (3-Tier Architecture)** tiêu chuẩn nhằm đảm bảo tính tách biệt, khả năng mở rộng và bảo mật. Thiết kế này tạo điều kiện cho luồng dữ liệu thông suốt giữa các tầng giao diện, ứng dụng và lưu trữ dữ liệu.

*   **Tầng Giao diện & Ứng dụng:** Vận hành bởi **Amazon EC2** với bộ LAMP stack (Linux, Apache, MySQL client, PHP) để xử lý các yêu cầu web và logic ứng dụng.
*   **Tầng Cơ sở dữ liệu:** Sử dụng **Amazon RDS (MySQL)** để quản lý dữ liệu có cấu trúc, bao gồm thông tin tài khoản người dùng và danh mục đĩa than.
*   **Tầng Lưu trữ:** Sử dụng **Amazon S3** để lưu trữ các tài sản truyền thông tĩnh và các tệp âm thanh chất lượng cao.

![Architecture](/images/4.2-Architecture/architecture.png)

### Lựa chọn dịch vụ và Lý do

Việc lựa chọn các dịch vụ dựa trên tiêu chí về độ tin cậy, khả năng quản lý và tối ưu hóa chi phí:

*   **Amazon EC2 (t3.micro):** Được chọn nhờ tính linh hoạt trong cấu hình môi trường và thuộc phạm vi AWS Free Tier, giúp giảm thiểu chi phí vận hành.
*   **Amazon RDS (MySQL):** Cung cấp giải pháp cơ sở dữ liệu được quản lý, tự động hóa việc sao lưu và vá lỗi, đảm bảo tính toàn vẹn dữ liệu cho nền tảng thương mại điện tử.
*   **Amazon S3:** Được lựa chọn nhờ độ bền cao và khả năng cung cấp các tệp dữ liệu lớn trực tiếp qua URL công khai, giảm tải cho máy chủ web.

### Bảo mật và Tuân thủ

*   **Bảo mật mạng:** Các Nhóm bảo mật (Security Groups) đóng vai trò như tường lửa ảo để kiểm soát lưu lượng truy cập. Chỉ các cổng thiết yếu (80 cho HTTP, 443 cho HTTPS và 22 cho SSH) được cấp phép mở.
*   **Quản lý truy cập:** Các vai trò (Roles) và chính sách (Policies) IAM được cấu hình theo nguyên tắc **Quyền hạn tối thiểu (Least Privilege)**, đảm bảo các dịch vụ chỉ có các quyền cần thiết để thực hiện tác vụ cụ thể.
*   **Bảo vệ dữ liệu:** Không có thông tin xác thực nhạy cảm hoặc mã khóa truy cập (Access Keys) nào được nhúng trực tiếp trong mã nguồn ứng dụng.