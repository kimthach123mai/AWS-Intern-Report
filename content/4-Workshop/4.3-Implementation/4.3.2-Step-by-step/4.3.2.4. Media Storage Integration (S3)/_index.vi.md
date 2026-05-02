---
title: "Tích hợp lưu trữ Media (S3)"
weight: 4
pre: "<b> 4.3.2.4. </b>"
---

### Mục tiêu
Chuyển các tài sản tĩnh và tệp âm thanh chất lượng cao từ máy chủ web sang **Amazon S3** nhằm cải thiện hiệu suất và khả năng mở rộng của ứng dụng.

### Các bước thực hiện

#### 1. Khởi tạo S3 Bucket
*   **Dịch vụ:** Truy cập **S3 Dashboard** và chọn **Create bucket**.
*   **Tên Bucket:** `classic-groove-media-assets` (Tên phải là duy nhất trên toàn cầu).
*   **Khu vực:** Chọn **ap-southeast-2 (Sydney)** để đồng bộ với thực thể EC2.
*   **Quyền sở hữu đối tượng:** Kích hoạt **ACLs enabled** để quản lý quyền hạn của từng tệp tin.
*   **Chặn truy cập công khai:** Bỏ chọn "Block all public access" để cho phép hiển thị hình ảnh và âm thanh ra bên ngoài.

#### 2. Quản lý danh tính và truy cập (IAM)
Để cho phép thực thể EC2 tải tệp lên S3 một cách an toàn:
*   **Tạo người dùng IAM:** Tạo người dùng tên là `classic-groove-s3-admin`.
*   **Gán chính sách:** Chỉ định quyền `AmazonS3FullAccess`.
*   **Thông tin xác thực:** Khởi tạo và lưu lại **Access Key ID** cùng **Secret Access Key**.

#### 3. Tích hợp vào ứng dụng
*   **Cài đặt SDK:** Sử dụng **Composer** trên máy chủ EC2 để cài đặt AWS SDK cho PHP:
    ```bash
    composer require aws/aws-sdk-php
    ```
*   **Cấu hình mã nguồn:** Cập nhật logic lưu trữ của ứng dụng để sử dụng S3 client:
    ```php
    $s3Client = new Aws\S3\S3Client([
        'region'  => 'ap-southeast-2',
        'version' => 'latest',
        'credentials' => [
            'key'    => 'YOUR_ACCESS_KEY',
            'secret' => 'YOUR_SECRET_KEY',
        ],
    ]);
    ```

#### 4. Di chuyển dữ liệu
*   Tải các ảnh bìa album đĩa than và các bản nghe thử từ máy cục bộ lên S3 bucket thông qua AWS Console hoặc AWS CLI.
*   Cập nhật các bản ghi trong cơ sở dữ liệu RDS để trỏ đường dẫn tới URL của đối tượng trên S3.