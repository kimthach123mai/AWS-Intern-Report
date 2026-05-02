---
title: "Kiểm thử và Giám sát"
date: 2026-05-01
weight: 4
chapter: false
pre: "<b> 4.4. </b>"
---

### Xác minh hệ thống

Sau khi triển khai hạ tầng đám mây, một loạt các bài kiểm tra toàn diện được thực hiện để đảm bảo ứng dụng **Classic Groove** vận hành trơn tru trên tất cả các tầng dịch vụ của AWS.

#### 1. Kiểm thử chức năng toàn diện
*   **Khả năng truy cập Web:** Xác minh cửa hàng có thể truy cập được thông qua Elastic IP và Public DNS trên các cổng web tiêu chuẩn.
*   **Truyền phát đa phương tiện:** Xác nhận các bản nghe thử âm thanh chất lượng cao được cung cấp trực tiếp từ Amazon S3 mà không gặp lỗi trễ hay lỗi phân quyền.
*   **Logic giao dịch:** Kiểm tra các thao tác CRUD (Thêm, Đọc, Sửa, Xóa) cho kho đĩa than và giỏ hàng, đảm bảo dữ liệu được lưu trữ bền vững trong Amazon RDS.

#### 2. Kiểm tra Bảo mật và Kết nối
*   **Cô lập cơ sở dữ liệu:** Xác nhận thực thể RDS không thể bị truy cập trực tiếp từ internet công cộng, bắt buộc phải thông qua máy chủ web EC2 làm trung gian.
*   **Xác minh IAM:** Kiểm tra việc thực thể EC2 sử dụng các vai trò đã gán để giao tiếp với S3, loại bỏ hoàn toàn việc nhúng thông tin xác thực vào mã nguồn.

#### 3. Giám sát vận hành
*   **Sử dụng tài nguyên:** Theo dõi mức sử dụng CPU và bộ nhớ của thực thể `t3.micro` để đảm bảo tính ổn định khi mô phỏng lưu lượng truy cập cao.
*   **Giám sát chi phí:** Thường xuyên kiểm tra AWS Billing Dashboard để đảm bảo chi phí duy trì ở mức ước tính khoảng **$5.81/tháng**.

---

> **Kết luận:** Giai đoạn kiểm thử xác nhận rằng việc tích hợp giữa các tầng tính toán, cơ sở dữ liệu và lưu trữ đã thành công, tạo ra một môi trường ổn định cho thị trường âm nhạc số.