---
title: "Định dạng dự án và Công cụ"
date: 2026-05-01
weight: 1
chapter: false
pre: "<b> 4.1. </b>"
---

### Định dạng dự án

Phần workshop được trình bày dưới dạng tài liệu hướng dẫn kỹ thuật chuyên sâu, tuân thủ phương pháp triển khai theo từng bước cụ thể. Nội dung được tổ chức nhằm cung cấp một lộ trình rõ ràng để tái lập hạ tầng điện toán đám mây cho dự án **Classic Groove** trên nền tảng AWS.

Tài liệu tuân thủ các tiêu chuẩn báo cáo chuyên nghiệp, được chia thành các phần logic: Tổng quan, Thiết kế kiến trúc, Các bước triển khai và Kiểm thử sau triển khai. Nhằm đảm bảo khả năng tiếp cận và tính rõ ràng về mặt kỹ thuật, báo cáo được duy trì dưới định dạng song ngữ (Tiếng Anh và Tiếng Việt).

### Công cụ và Yêu cầu

Quá trình triển khai sử dụng kết hợp hạ tầng đám mây và các công cụ phát triển để đáp ứng mục tiêu dự án:

*   **Nội dung song ngữ:** Tích hợp đầy đủ tiếng Anh và tiếng Việt để đảm bảo tính hoàn thiện của tài liệu.
*   **Quy trình cấu trúc:** Luồng nội dung xuyên suốt từ Bản đề xuất, Nhật ký công việc đến Workshop kỹ thuật và Tự đánh giá.
*   **Trực quan hóa kiến trúc:** Sử dụng các sơ đồ kỹ thuật mô tả sự tương tác giữa tầng giao diện web và các lớp lưu trữ dữ liệu.
*   **Dữ liệu kỹ thuật:** Bao gồm các kịch bản triển khai SQL, chuỗi kết nối PHP sử dụng SSL và cấu hình chính sách IAM.
*   **Các dịch vụ AWS sử dụng:** Vận hành kiến trúc đa dịch vụ bao gồm:
    *   **Amazon EC2:** Lưu trữ và vận hành logic ứng dụng web.
    *   **Amazon RDS (MySQL):** Cơ sở dữ liệu quan hệ được quản lý để lưu trữ thông tin kho hàng và người dùng.
    *   **Amazon S3:** Lưu trữ đối tượng có khả năng mở rộng cho các tệp âm thanh chất lượng cao và dữ liệu truyền thông.