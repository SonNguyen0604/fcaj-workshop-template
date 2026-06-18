---
title: "Các bài blogs đã dịch"
date: 2026-06-16
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Tại đây sẽ là phần liệt kê, giới thiệu các blogs mà các bạn đã dịch. Ví dụ:

###  [Blog 1 - Từ Cache Theo Giờ Đến Real-Time Pricing: Samsung Giải Quyết Bài Toán Đồng Bộ Giá Với AWS Lambda Response Streaming](3.1-Blog1/)
Bài viết này chia sẻ một case study thú vị từ AWS Architecture Blog về cách Samsung cải tiến hệ thống định giá trên Samsung.com để giải quyết bài toán đồng bộ dữ liệu theo thời gian thực. Bạn sẽ hiểu được những hạn chế của kiến trúc cũ sử dụng bộ nhớ cache qua Cron Job (như bùng nổ tổ hợp biến thể sản phẩm và độ trễ đồng bộ lên tới 60 phút), lý do vì sao Samsung quyết định loại bỏ hoàn toàn tầng trung gian này để chuyển sang mô hình Serverless, và cách kết hợp giữa Amazon CloudFront với AWS Lambda Response Streaming giúp giảm Time To First Byte (TTFB), đảm bảo hiển thị giá chính xác từ Source of Truth mà vẫn tối ưu được hiệu năng ở quy mô lớn.

###  [Blog 2 - ...](3.2-Blog2/)
Blog này giới thiệu cách bắt đầu xây dựng data lake trong lĩnh vực y tế bằng cách áp dụng kiến trúc microservices. Bạn sẽ tìm hiểu vì sao data lake quan trọng trong việc lưu trữ và phân tích dữ liệu y tế đa dạng (hồ sơ bệnh án điện tử, dữ liệu xét nghiệm, thiết bị IoT y tế…), cách microservices giúp hệ thống linh hoạt, dễ mở rộng và dễ bảo trì hơn. Bài viết cũng hướng dẫn các bước khởi tạo môi trường, tổ chức pipeline xử lý dữ liệu, và đảm bảo tuân thủ các tiêu chuẩn bảo mật & quyền riêng tư như HIPAA.
###  [Blog 3 - ...](3.3-Blog3/)

Blog này giới thiệu cách bắt đầu xây dựng data lake trong lĩnh vực y tế bằng cách áp dụng kiến trúc microservices. Bạn sẽ tìm hiểu vì sao data lake quan trọng trong việc lưu trữ và phân tích dữ liệu y tế đa dạng (hồ sơ bệnh án điện tử, dữ liệu xét nghiệm, thiết bị IoT y tế…), cách microservices giúp hệ thống linh hoạt, dễ mở rộng và dễ bảo trì hơn. Bài viết cũng hướng dẫn các bước khởi tạo môi trường, tổ chức pipeline xử lý dữ liệu, và đảm bảo tuân thủ các tiêu chuẩn bảo mật & quyền riêng tư như HIPAA.

