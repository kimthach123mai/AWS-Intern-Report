---
title: "Cấu hình Cơ sở dữ liệu (RDS)"
weight: 3
pre: "<b>4.3.2.3. </b>"
---

### Mục tiêu
Triển khai một thực thể cơ sở dữ liệu MySQL được quản lý để xử lý dữ liệu có cấu trúc cho nền tảng **Classic Groove**, đảm bảo tính sẵn sàng cao và toàn vẹn dữ liệu.

### Các bước thực hiện

#### 1. Khởi tạo thực thể RDS
*   **Dịch vụ:** Truy cập **RDS Dashboard** và chọn **Create database**.
*   **Lựa chọn Engine:** Chọn **MySQL**.
*   **Templates:** Chọn **Free Tier** để tối ưu hóa chi phí.
*   **Cài đặt:**
    *   **DB instance identifier:** `classic-groove-db`.
    *   **Master username:** `admin`.
    *   **Master password:** Thiết lập mật khẩu bảo mật.
*   **Cấu hình thực thể:** Chọn loại máy chủ `db.t3.micro`.
*   **Kết nối:**
    *   **Public access:** Chọn **Yes** (phục vụ cấu hình ban đầu và di chuyển dữ liệu).
    *   **VPC Security Group:** Tạo nhóm mới tên là `classic-groove-db-sg`.
*   **Cấu hình bổ sung:**
    *   **Initial database name:** `classic_groove`.

#### 2. Cấu hình bảo mật
Để cho phép máy chủ web EC2 giao tiếp với cơ sở dữ liệu:
*   Truy cập **Security Group** `classic-groove-db-sg`.
*   Thêm **Inbound Rule**:
    *   **Loại:** MySQL/Aurora (Cổng 3306).
    *   **Nguồn (Source):** Chọn ID Nhóm bảo mật của thực thể EC2 hoặc `0.0.0.0/0` để kiểm thử.

#### 3. Kết nối và Di chuyển dữ liệu
*   **Cài đặt MySQL Client trên EC2:**
    ```bash
    sudo dnf install mysql -y
    ```
*   **Kết nối tới RDS:**
    ```bash
    mysql -h <rds-endpoint> -u admin -p
    ```
*   **Nhập dữ liệu (Import):** Chuyển tệp SQL từ máy cục bộ và nhập vào thực thể RDS:
    
```bash
    mysql -h <rds-endpoint> -u admin -p classic_groove < classic-groove.sql
```

#### 4. Tích hợp ứng dụng
Cập nhật tệp cấu hình PHP (ví dụ: `dataProvider.php`) để trỏ đến endpoint của RDS:
```php
mysqli_real_connect(
    $connection,
    "classic-groove-db.<id>.<region>.rds.amazonaws.com",
    "admin",
    "your_password",
    "classic_groove",
    3306
);
```