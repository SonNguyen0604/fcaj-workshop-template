---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Mục tiêu Tuần 7:

* Triển khai ứng dụng trên Docker: Đi sâu vào đóng gói ứng dụng đa container (multi-container), triển khai môi trường local và tích hợp kiến trúc đám mây AWS.
* Quản lý & Triển khai Container: Xây dựng, quản lý và triển khai các ứng dụng phần mềm sử dụng Docker container, Docker Compose và các thực thể Amazon EC2.
* Tích hợp Kho chứa Image & Cơ sở dữ liệu: Khởi tạo và cấu hình kho lưu trữ container trên Amazon ECR, Docker Hub và kết nối ứng dụng với Amazon RDS (MySQL) trong các nhóm bảo mật VPC biệt lập.


### Các công việc cần thực hiện trong tuần này:
<table>
  <thead>
    <tr>
      <th>Ngày</th>
      <th>Công việc</th>
      <th>Ngày bắt đầu</th>
      <th>Ngày hoàn thành</th>
      <th>Tài liệu tham khảo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2</td>
      <td>
      <ul>
        <li>
            Triển khai trên môi trường Local (Deploy on Local)
            <ul>
              <li>Cài đặt các gói phụ thuộc (Install Dependencies)</li>
              <li>Triển khai ứng dụng (Deploy Application)</li>
              <li>Kiểm thử ứng dụng (Test Application)</li>
            </ul>
          </li>
          </ul>
      </td>
      <td>01/06/2026</td>
      <td>01/06/2026</td>
      <td>
        <a href="https://000015.awsstudygroup.com/">https://000015.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Chuẩn bị & Thiết lập hạ tầng
            <ul>
                <li>Các bước chuẩn bị (Preparation)</li>
                <li>Khởi chạy thực thể RDS (Launch RDS Instance)</li>
                <li>Cấu hình thực thể EC2 (Configuring EC2 Instance)</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>02/06/2026</td>
      <td>02/06/2026</td>
      <td>
      <a href="https://000015.awsstudygroup.com/">https://000015.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Triển khai chỉ sử dụng Docker Image (Deploy use only Docker Image)
            <ul>
              <li>6.1. Triển khai ứng dụng (Nginx, Frontend, Backend Container)</li>
              <li>6.2. Kiểm thử ứng dụng kết nối với Amazon RDS (MySQL)</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>03/06/2026</td>
      <td>03/06/2026</td>
      <td><a href="https://000015.awsstudygroup.com/">https://000015.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Triển khai với Docker Compose (Deploy with Docker Compose)
              <ul>
                <li>7.1. Triển khai ứng dụng sử dụng Docker Compose & Docker Daemon</li>
                <li>7.2. Kiểm thử hệ thống ứng dụng đa container</li>
              </ul>
          </li>
        </ul>
      </td>
      <td>04/06/2026</td>
      <td>04/06/2026</td>
      <td><a href="https://000015.awsstudygroup.com/">https://000015.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>
            Đẩy Image lên kho chứa & Dọn dẹp tài nguyên
               <ul>
                <li>8.1. Sử dụng ECR (Khởi tạo kho chứa cho Frontend Image)</li>
                <li>8.2. Sử dụng Docker Hub</li>
                <li>9. Dọn dẹp tài nguyên (Clean Up Resources)</li>
              </ul>
          </li>
        </ul>
      </td>
      <td>05/06/2026</td>
      <td>05/06/2026</td>
      <td><a href="https://000015.awsstudygroup.com/">https://000015.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>


### KẾT QUẢ ĐẠT ĐƯỢC TUẦN 6: WORKSHOP TRIỂN KHAI ỨNG DỤNG TRÊN DOCKER

1. **Đóng gói Container cục bộ & Kiểm thử Ứng dụng**
   - **Cô lập môi trường:** Đánh giá và hiểu rõ lợi ích của việc triển khai ứng dụng trên nền tảng Docker container thay vì chạy trực tiếp trên hệ điều hành máy tính cá nhân.
   - **Xác thực hệ thống:** Đóng gói container thành công và kiểm thử hệ thống ứng dụng đa tầng bao gồm trình duyệt Client, Nginx Server, các Web Server ứng dụng (React/Node.js) và Database Engine.

2. **Kiến trúc đám mây & Đường ống lưu trữ Container**
   - **Khởi tạo Compute & Database:** Cấu hình thành công nút máy chủ Amazon EC2 và triển khai hệ quản trị cơ sở dữ liệu Amazon RDS (MySQL) nằm cô lập trong một Private Subnet Group.
   - **Phân tách an ninh mạng:** Điều phối luồng lưu lượng truy cập qua AWS VPC Internet Gateway, thiết lập các Nhóm bảo mật (Security Groups) riêng biệt cho vùng Public SG (máy chủ EC2) và vùng Private DB SG (RDS).

3. **Điều phối đa Container & Quản lý Kho chứa Image**
   - **Tối ưu hóa với Docker Compose:** Chuẩn hóa quy trình vận hành và quản lý các nhóm container (Container Group) trực tiếp thông qua cấu hình Docker Compose và Docker Daemon.
   - **Quản lý sản phẩm đóng gói:** Thiết lập luồng phân phối ứng dụng bằng cách đẩy (push) các Docker image đã xác thực lên các kho lưu trữ từ xa bao gồm Amazon Elastic Container Registry (ECR) và Docker Hub.