---
title: "Điều kiện tiên quyết"
date: 2026-05-01
weight: 1
chapter: false
pre: "<b> 4.3.1. </b>"
---

### Yêu cầu về môi trường

Trước khi bắt đầu quá trình triển khai cho **Classic Groove**, các điều kiện tiên quyết về kỹ thuật sau đây phải được thiết lập để đảm bảo việc tích hợp các dịch vụ AWS diễn ra suôn sẻ.

#### 1. Tài khoản hạ tầng đám mây
*   **AWS Management Console:** Bắt buộc phải có quyền truy cập vào một tài khoản AWS đang hoạt động.
*   **Khu vực triển khai (Region):** Hệ thống được chuẩn hóa trên khu vực **ap-southeast-2 (Sydney)** để đảm bảo tính nhất quán và sẵn có của dịch vụ.

#### 2. Công cụ và Kết nối cục bộ
*   **Giao diện dòng lệnh:** Sử dụng SSH client (như Git Bash hoặc Terminal) để quản lý máy chủ từ xa một cách an toàn.
*   **Truyền tải dữ liệu:** Sử dụng giao thức Secure Copy (SCP) để di chuyển mã nguồn lên môi trường đám mây.
*   **Quản lý thư viện:** Cần cài đặt **Composer** để quản lý AWS SDK cho PHP, cho phép kết nối giữa EC2 và S3.

#### 3. Cấu hình bảo mật và IAM
Quá trình triển khai yêu cầu các quyền **IAM (Identity and Access Management)** cụ thể để quản lý tài nguyên theo nguyên tắc quyền hạn tối thiểu:
*   Quyền truy cập đầy đủ (Full Access) cho các dịch vụ EC2, RDS và S3.
*   Quyền khởi tạo Access Keys cho việc xác thực ở cấp độ ứng dụng.