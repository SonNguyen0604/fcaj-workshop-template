---
title: "Bài viết Blogs"
date: 2026-06-22
weight: 3
chapter: false
pre: " <b> 3.1. </b> "
---

# DANH SÁCH CÁC BÀI BLOGS CHIA SẺ KẾ THỪA (AWS STUDY GROUP)

Theo yêu cầu của chương trình First Cloud Journey, nhóm chúng tôi thực hiện nghiên cứu, biên dịch và chia sẻ 3 bài viết chuyên sâu về kỹ thuật lên cộng đồng AWS Study Group nhằm lan tỏa kiến thức cốt lõi về tính sẵn sàng cao.

---

## 📝 BÀI BLOG 1: Tổng quan về kiến trúc High Availability và cơ chế Multi-AZ trên AWS

* **Trạng thái:** Dự kiến đăng vào Tuần 2 (Mục tiêu lan tỏa kiến thức nền tảng).
* **Nội dung chính:**
  * Khái niệm cốt lõi về High Availability (Tính sẵn sàng cao) và Fault Tolerance (Khả năng chống chịu lỗi). Phân biệt rõ sự khác nhau giữa hai khái niệm này để tránh nhầm lẫn khi thiết kế hệ thống production.
  * Tầm quan trọng của AWS Global Infrastructure: Khái niệm về AWS Regions (Vùng) và AWS Availability Zones (AZ - Khu vực sẵn sàng). Vì sao thiết kế ứng dụng trên một AZ đơn lẻ luôn tiềm ẩn rủi ro Single Point of Failure (SPOF).
  * Cách thức hoạt động của cơ chế Multi-AZ: Phân bổ tài nguyên máy chủ EC2 một cách độc lập qua các trung tâm dữ liệu có nguồn điện, mạng và làm mát tách biệt nhằm cô lập hoàn toàn các sự cố vật lý.

---

## 📝 BÀI BLOG 2: Tối ưu hóa hạ tầng tự động co giãn với Application Load Balancer và Auto Scaling Group

* **Trạng thái:** Dự kiến đăng vào Tuần 3 (Giai đoạn triển khai hạ tầng kỹ thuật chính).
* **Nội dung chính:**
  * Giới thiệu về Application Load Balancer (ALB): Cơ chế tiếp nhận lưu lượng truy cập từ Internet, kiểm tra sức khỏe hệ thống (Health Checks) và phân phối thông minh các request xuống các máy chủ lành mạnh ở các AZ khác nhau.
  * Sức mạnh của AWS Auto Scaling Group (ASG): Cách thiết lập các chính sách co giãn tự động (Scaling Policies) dựa trên các chỉ số thực tế như phần trăm CPU tiêu thụ hoặc số lượng request.
  * Sự kết hợp end-to-end giữa ALB và ASG: Giúp hệ thống không những tự động phục hồi khi có máy chủ bị sập (Self-healing) mà còn tối ưu hóa chi phí bằng cách tự động tắt bớt máy chủ khi lượng truy cập thấp.

---

## 📝 BÀI BLOG 3: Bảo mật dữ liệu Multi-AZ với Amazon RDS và Giám sát tập trung bằng Amazon CloudWatch

* **Trạng thái:** Dự kiến đăng vào Tuần 4 (Giai đoạn kiểm thử và đo lường hệ thống).
* **Nội dung chính:**
  * Giải pháp lưu trữ dữ liệu bền vững với Amazon RDS Multi-AZ: Cơ chế đồng bộ hóa dữ liệu theo thời gian thực (Synchronous Replication) từ cơ sở dữ liệu chính (Primary DB) sang cơ sở dữ liệu dự phòng (Standby DB) ở một Availability Zone khác.
  * Quy trình tự động chuyển vùng sự cố (Automated Failover): Khi DB chính gặp lỗi phần cứng hoặc sập AZ, Amazon RDS tự động chuyển đổi định danh sang DB dự phòng mà không làm gián đoạn kết nối của ứng dụng Python phía trên.
  * Giám sát toàn diện với Amazon CloudWatch: Cách thiết lập Dashboard theo dõi tài nguyên, cấu hình CloudWatch Alarms để tự động gửi thông báo cảnh báo qua email khi hệ thống gặp tải cao hoặc có sự cố failover xảy ra.
