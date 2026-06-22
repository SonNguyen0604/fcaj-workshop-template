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
  * `[Thành viên 3: Chèn code block Dockerfile/Python kết nối DB vào đây]`
* **Hình ảnh minh họa:**
  
  `[Thành viên 3: Chèn hình ảnh log container chạy thành công tại đây]`

#### **Bước 4: Cấu hình Application Load Balancer & Auto Scaling Group**
* **Nội dung:** Tạo Target Group, cấu hình Application Load Balancer (ALB) tại Public Subnet. Thiết lập Auto Scaling Group (ASG) dựa trên Launch Template với chính sách co giãn tự động dựa trên CPU.
* **Hình ảnh minh họa:**
  
  `[Thành viên 4: Chèn hình ảnh cấu hình ALB, ASG và Scaling Policies tại đây]`

#### **Bước 5: Thiết lập Hệ thống giám sát Amazon CloudWatch**
* **Nội dung:** Cấu hình CloudWatch Logs Agent để thu thập log hệ thống, thiết lập CloudWatch Dashboard theo dõi hiệu năng và tạo Alarm cảnh báo.
* **Hình ảnh minh họa:**
  
  `[Thành viên 5: Chèn hình ảnh giao diện CloudWatch Dashboard và Alarms tại đây]`

---

### 4. Kiểm thử hệ thống & Giả lập sự cố Failover (Testing & Validation)

Quy trình xác thực tính sẵn sàng cao của hệ thống khi xảy ra sự cố:
1. **Kiểm thử tải (Load Test):** Giả lập lượng request tăng đột biến để kiểm tra xem Auto Scaling Group có tự động scale-out tăng số lượng EC2 lên hay không.
2. **Giả lập sự cố (Failover Test):** Tiến hành tắt đột ngột (Terminate) toàn bộ các Instance EC2 nằm trong Availability Zone A (AZ-A).
3. **Kết quả mong đợi:** Application Load Balancer lập tức nhận diện sự cố qua Health Check, tự động ngắt định tuyến traffic tới AZ-A và chuyển hướng 100% người dùng sang các máy chủ dự phòng ở AZ-B một cách mượt mà, không gây gián đoạn dịch vụ.
4. **Minh chứng hệ thống phục hồi:**
  
  `[Thành viên 5: Chèn hình ảnh log/metric CloudWatch chứng minh hệ thống tự phục hồi tại đây]`

---

### 5. Dọn dẹp tài nguyên (Clean-up)

Thực hiện xóa toàn bộ tài nguyên theo thứ tự sau để tránh phát sinh chi phí ngoài ý muốn trên tài khoản AWS:
1. Xóa Auto Scaling Group và Application Load Balancer.
2. Xóa các EC2 Instances (Terminate).
3. Xóa Cơ sở dữ liệu Amazon RDS và dọn dẹp Amazon S3 Bucket.
4. Xóa tài nguyên mạng Amazon VPC.
