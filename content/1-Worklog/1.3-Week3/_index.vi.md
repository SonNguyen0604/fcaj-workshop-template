---
title: "Worklog Tuần 3"
date: 2026-04-27
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Quản lý EC2 & hệ điều hành: triển khai và vận hành Windows/Linux instances, EBS snapshots và custom AMIs
* Triển khai web & ứng dụng: thiết lập môi trường LAMP, Node.js và XAMPP để chạy ứng dụng User Management
* Lưu trữ & CSDL: cấu hình Amazon S3 cho static hosting và kiến trúc RDS/Lightsail cho các giải pháp dữ liệu được quản lý

### Các công việc cần triển khai trong tuần này:

<table>
  <thead>
    <tr>
      <th>Thứ</th>
      <th>Công việc</th>
      <th>Ngày bắt đầu</th>
      <th>Ngày hoàn thành</th>
      <th>Nguồn tài liệu</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2</td>
      <td>
        <ul>
          <li>Khởi chạy Microsoft Windows Server Instance</li>
          <li>Khởi chạy Amazon Linux Instance</li>
          <li>
            Tìm hiểu Amazon Elastic Compute Cloud (EC2)
            <ul>
              <li>Thay đổi EC2 Instance Type</li>
              <li>Tạo và quản lý EBS Snapshots</li>
              <li>Tạo Custom AMI</li>
              <li>Khởi chạy instance từ Custom AMI</li>
              <li>Khôi phục quyền truy cập Windows Instances</li>
              <li>Khôi phục quyền truy cập Linux Instances</li>
              <li>Remote Desktop tới EC2 Ubuntu</li>
              <li>Kiến trúc Amazon EBS Snapshots</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>27/04/2026</td>
      <td>27/04/2026</td>
      <td>
        <a href="https://000004.awsstudygroup.com/3-launchwindowsinstance/">https://000004.awsstudygroup.com/3-launchwindowsinstance/</a><br>
        <a href="https://000004.awsstudygroup.com/4-launchlinuxinstance/">https://000004.awsstudygroup.com/4-launchlinuxinstance/</a><br>
        <a href="https://000004.awsstudygroup.com/5-amazonec2basic/">https://000004.awsstudygroup.com/5-amazonec2basic/</a><br>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Triển khai AWS User Management Application trên Amazon Linux
            <ul>
              <li>Cài đặt LAMP Web Server trên Amazon Linux</li>
              <li>Cài đặt Nodejs trên Amazon Linux</li>
              <li>Triển khai ứng dụng trên Linux Instance</li>
            </ul>
          </li>
          <li>
            Triển khai Nodejs Application trên Amazon EC2
            <ul>
              <li>Cài đặt XAMPP trên Windows Instance</li>
              <li>Cài đặt Nodejs trên Windows Instance</li>
              <li>Triển khai AWS User Management Application trên Windows Server</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>28/04/2026</td>
      <td>28/04/2026</td>
      <td>
        <a href="https://000004.awsstudygroup.com/6-awsfcjmanagement-linux/">https://000004.awsstudygroup.com/6-awsfcjmanagement-linux/</a><br>
        <a href="https://000004.awsstudygroup.com/7-awsfcjmanagement-windows/">https://000004.awsstudygroup.com/7-awsfcjmanagement-windows/</a>
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Amazon S3
            <ul>
              <li>Tạo S3 Bucket</li>
              <li>Cấu hình Public Access Block</li>
              <li>Cấu hình Public Objects</li>
              <li>Kiểm thử Website</li>
              <li>Tăng tốc static website với CloudFront</li>
              <li>Bật Bucket Versioning</li>
              <li>Sao chép đối tượng đa vùng (Multi-Region Replication)</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>29/04/2026</td>
      <td>29/04/2026</td>
      <td><a href="https://000057.awsstudygroup.com/">https://000057.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Amazon RDS
            <ul>
              <li>Tạo VPC, EC2 Security Group, RDS Security Group, DB Subnet Group</li>
              <li>Tạo EC2 Instance</li>
              <li>Tạo RDS Database Instance</li>
              <li>Triển khai ứng dụng</li>
              <li>Backup và Restore</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>30/04/2026</td>
      <td>30/04/2026</td>
      <td><a href="https://000005.awsstudygroup.com/">https://000005.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Amazon Lightsail
            <ul>
              <li>Triển khai Database trên Lightsail</li>
              <li>Triển khai WordPress trên Lightsail</li>
              <li>Triển khai Prestashop E-commerce Instance</li>
              <li>Triển khai Akauning Instance</li>
              <li>Bảo mật ứng dụng</li>
              <li>Tạo Snapshot</li>
              <li>Tạo Alarm</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>01/05/2026</td>
      <td>01/05/2026</td>
      <td><a href="https://000045.awsstudygroup.com/">https://000045.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>

### THÀNH TỰU TUẦN 3: TRIỂN KHAI ĐA NỀN TẢNG & QUẢN LÝ DỮ LIỆU

1. **Vận hành EC2 nâng cao & quản trị hệ điều hành**
   - **Vòng đời instance:** Làm chủ triển khai đa hệ điều hành (Amazon Linux, Ubuntu, Windows Server) và thay đổi instance type để tối ưu hiệu năng.
   - **Sao lưu & khôi phục:** Triển khai cơ chế DR (disaster recovery) bằng EBS Snapshots và Custom AMIs để nhân bản môi trường nhanh chóng.

2. **Lưu trữ ứng dụng full-stack**
   - **Cấu hình web stack:** Triển khai thành công các ứng dụng User Management bằng môi trường LAMP (Linux, Apache, MySQL, PHP) và Node.js.
   - **Triển khai đa nền tảng:** Tích hợp XAMPP trên Windows Server và quản lý kết nối ứng dụng qua MobaXterm và Remote Desktop.

3. **Lưu trữ mở rộng & phân phối nội dung**
   - **Làm chủ Amazon S3:** Cấu hình S3 buckets với các tính năng nâng cao gồm Public Access Blocks, Versioning và Multi-Region Replication.
   - **Tăng tốc biên (edge):** Tối ưu phân phối static website bằng cách tích hợp S3 với Amazon CloudFront để truy cập toàn cầu độ trễ thấp.

4. **CSDL được quản lý & triển khai nhanh**
   - **CSDL quan hệ (RDS):** Thiết kế cụm cơ sở dữ liệu an toàn trong custom VPC Subnet Groups và thực hiện backup/restore tự động.
   - **Amazon Lightsail:** Sử dụng Lightsail để triển khai đơn giản WordPress và các instance E-commerce (Prestashop), kèm monitoring và alarms.

   ![w3_d1_1](/images/1-Worklog/w3_d1_1.png)
   ![w3_d1_2](/images/1-Worklog/w3_d1_2.png)
   ![w3_d2_3](/images/1-Worklog/w3_d2_3.png)
   ![w3_d1_3](/images/1-Worklog/w3_d1_3.png)
   ![w3_d1_4](/images/1-Worklog/w3_d1_4.png)
   ![w3_d1_5](/images/1-Worklog/w3_d1_5.png)
   ![w3_d1_6](/images/1-Worklog/w3_d1_6.png)
   ![w3-d1-1](/images/1-Worklog/w3-d1-1.jpg)