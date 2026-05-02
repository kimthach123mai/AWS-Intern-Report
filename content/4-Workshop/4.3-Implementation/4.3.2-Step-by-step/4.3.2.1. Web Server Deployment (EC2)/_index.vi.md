---
title: "Triển khai máy chủ Web"
weight: 1
pre: "<b> 4.3.2.1. </b>"
---

### Mục tiêu
Khởi tạo một máy chủ ảo trên AWS để lưu trữ và vận hành logic ứng dụng PHP cho cửa hàng **Classic Groove**.

### Các bước thực hiện

#### 1. Khởi tạo Instance
*   **Dịch vụ:** Truy cập **EC2 Dashboard** và chọn **Launch Instance**.
*   **Tên máy chủ:** `classic-groove-server`.
*   **Hệ điều hành:** Chọn **Amazon Linux 2023** (hoặc Amazon Linux 2).
*   **Loại máy chủ:** `t3.micro` (Thuộc phạm vi Free Tier).

#### 2. Bảo mật truy cập
*   **Cặp khóa (Key Pair):** Khởi tạo cặp khóa mới có tên `aws-key.pem`.
*   **Nhóm bảo mật (Security Group):** Tạo nhóm mới và cho phép các lưu lượng truy cập sau:
    *   **SSH (Cổng 22):** Giới hạn cho IP quản trị cụ thể.
    *   **HTTP (Cổng 80):** Mở cho toàn bộ internet để truy cập web.
    *   **HTTPS (Cổng 443):** Mở để truy cập web bảo mật.

#### 3. Hoàn tất
*   Xác nhận cài đặt lưu trữ (Mặc định 8GB) và chọn **Launch Instance**.
*   Ghi lại địa chỉ **Public IPv4** để sử dụng cho các bước kết nối tiếp theo.