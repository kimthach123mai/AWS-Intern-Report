---
title: "Tối ưu hóa và Dọn dẹp"
date: 2026-05-01
weight: 5
chapter: false
pre: "<b> 4.5. </b>"
---

### Chiến lược Tối ưu hóa

Dự án **Classic Groove** được tối ưu hóa để cân bằng giữa hiệu suất vận hành và hiệu quả chi phí, đảm bảo chất lượng triển khai chuyên nghiệp trong phạm vi ngân sách sinh viên.

*   **Hiệu quả chi phí:** Việc sử dụng các thực thể `t3.micro` và `db.t3.micro` đảm bảo hạ tầng nằm trong giới hạn của AWS Free Tier ở mức tối đa có thể.
*   **Tinh chỉnh hiệu suất:** Các tài sản truyền thông được cung cấp trực tiếp từ Amazon S3, giúp giảm tải xử lý cho máy chủ web EC2 và cải thiện tốc độ tải trang cho các bản nghe thử âm thanh.
*   **Bảo mật tối ưu:** Truy cập được giới hạn thông qua Security Groups, chỉ cho phép các luồng dữ liệu cần thiết trên các cổng 80, 443 và 22. Các chính sách IAM tuân thủ nguyên tắc quyền hạn tối thiểu để bảo vệ tài nguyên đám mây.

---

### Quy trình Dọn dẹp tài nguyên

Để tránh các khoản phí không mong muốn sau khi dự án kết thúc, quy trình hủy bỏ tài nguyên được thực hiện một cách hệ thống:

1.  **Hủy cơ sở dữ liệu:** Xóa thực thể Amazon RDS `classic-groove-db`. Lưu ý: Đảm bảo bỏ chọn "Create final snapshot" trừ khi thực sự cần bản sao lưu cuối cùng.
2.  **Ngừng dịch vụ tính toán:** Hủy bỏ thực thể Amazon EC2 `classic-groove-server`. Hành động này sẽ tự động giải phóng các ổ lưu trữ EBS đi kèm.
3.  **Loại bỏ lưu trữ:** Làm trống và xóa S3 bucket `classic-groove-media-assets`. Tất cả ảnh bìa album và tệp âm thanh phải được xóa trước khi có thể xóa bucket.
4.  **Mạng và Bảo mật:** Xóa các Security Groups tùy chỉnh và giải phóng mọi địa chỉ Elastic IP đã cấp phát để tránh phí duy trì tài nguyên nhàn rỗi.

> **Ghi chú cuối:** Tuân thủ giao thức dọn dẹp này đảm bảo tài khoản AWS trở về trạng thái không phát sinh chi phí trong khi vẫn duy trì môi trường sạch cho các dự án tương lai.