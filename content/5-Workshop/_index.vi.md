---
title: "Xây dựng hệ thống High Availability"
date: 2026-06-22
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# WORKSHOP: ĐẢM BẢO TÍNH SẴN SÀNG CAO (HIGH AVAILABILITY) TRÊN AWS

Bài thực hành này hướng dẫn chi tiết quy trình thiết kế, triển khai và vận hành một hệ thống hạ tầng có khả năng chống chịu sự cố và tự động co giãn (Auto Scaling) trên nền tảng AWS cho ứng dụng Python.

---

### 1. Tổng quan & Sơ đồ kiến trúc (Overview & Architecture)

Hệ thống được thiết kế dựa trên các tiêu chuẩn tối ưu của AWS Well-Architected (Reliability Pillar), đảm bảo ứng dụng luôn sẵn sàng phục vụ người dùng ngay cả khi một trung tâm dữ liệu gặp sự cố vật lý nghiêm trọng.

* **Sơ đồ kiến trúc hệ thống:**
  
  `[Thành viên 2: Chèn hình ảnh sơ đồ vẽ từ Draw.io/Excalidraw tại đây]`

* **Các dịch vụ AWS sử dụng:** Amazon VPC, Application Load Balancer (ALB), Auto Scaling Group (ASG), Amazon EC2, Amazon RDS Multi-AZ, Amazon S3, Amazon CloudWatch.

---

### 2. Điều kiện tiên quyết (Prerequisites)

Để thực hiện bài Lab này, cần chuẩn bị:
* Tài khoản AWS đã được thiết lập quyền quản trị (IAM AdministratorAccess).
* AWS CLI và Docker Desktop đã được cài đặt ở môi trường máy trạm local.
* Mã nguồn ứng dụng demo viết bằng Python.

---

### 3. Các bước thực hiện chi tiết (Step-by-Step Guide)

#### **Bước 1: Khởi tạo hạ tầng mạng mạng VPC Multi-AZ**
* **Nội dung:** Cấu hình VPC chạy trên 2 Availability Zones độc lập (AZ-A và AZ-B). Mỗi AZ chia làm 1 Public Subnet (định tuyến ra Internet Gateway) và 1 Private Subnet.
* **Hình ảnh minh họa console VPC:**
  
  `[Thành viên 2: Chèn hình ảnh console VPC, Subnets và Route Tables tại đây]`

#### **Bước 2: Triển khai Cơ sở dữ liệu Amazon RDS Multi-AZ**
* **Nội dung:** Khởi tạo DB Instance nằm trong Private Subnet Subnet Group, bật tính năng Multi-AZ Deployment để tự động đồng bộ dữ liệu theo thời gian thực sang phân vùng dự phòng.
* **Hình ảnh minh họa cấu hình RDS:**
  
  `[Thành viên 2: Chèn hình ảnh thông số RDS Multi-AZ đang hoạt động tại đây]`

#### **Bước 3: Đóng gói và Triển khai ứng dụng Python trên EC2**
* **Nội dung:** Viết Dockerfile đóng gói ứng dụng Python, build image và chạy thử nghiệm trên EC2 Instance để kiểm tra kết nối tới RDS và S3.
* **Đoạn mã cấu hình (Code Snippet):**
  ```dockerfile
  # Dockerfile mẫu hoặc mã nguồn cấu hình kết nối ứng dụng
  # [Thành viên 3: Chèn code block Dockerfile/Python kết nối DB vào đây]
