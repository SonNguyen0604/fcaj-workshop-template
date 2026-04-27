---
title: "Worklog Tuần 2"
date: 2024-04-17
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Kiến thức nền tảng về AWS Networking & triển khai hạ tầng
* Xây dựng hạ tầng cloud an toàn: từ VPC Peering đến tích hợp Active Directory

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
          <li>
            Tìm hiểu Amazon VPC & kiến thức nền tảng về Networking
            <ul>
              <li>Tạo VPC</li>
              <li>Tạo Subnet</li>
              <li>Tạo Internet Gateway</li>
              <li>Tạo Route Table</li>
              <li>Tạo Security Group</li>
              <li>Bật VPC Flow Logs</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>22/04/2026</td>
      <td>22/04/2026</td>
      <td><a href="https://000003.awsstudygroup.com/3-prerequisite/">https://000003.awsstudygroup.com/3-prerequisite/</a></td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Triển khai Amazon EC2 Instances
            <ul>
              <li>Tạo EC2 Server</li>
              <li>Kiểm tra kết nối bằng VS Code</li>
              <li>Tạo NAT Gateway</li>
              <li>Tạo EC2 Instance Connect Endpoint</li>
              <li>CloudWatch Monitoring &amp; Alerting</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>23/04/2026</td>
      <td>23/04/2026</td>
      <td><a href="https://000003.awsstudygroup.com/4-createec2server/">https://000003.awsstudygroup.com/4-createec2server/</a></td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Tìm hiểu thiết lập Site-to-Site VPN Connection trên AWS
            <ul>
              <li>Tạo môi trường VPN</li>
              <li>Cấu hình VPN Connection</li>
              <li>VPN Connection dùng Strongswan với Transit Gateway</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>24/04/2026</td>
      <td>24/04/2026</td>
      <td><a href="https://000003.awsstudygroup.com/5-vpnsitetosite/">https://000003.awsstudygroup.com/5-vpnsitetosite/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Tìm hiểu triển khai Microsoft Active Directory trên AWS
            <ul>
              <li>Chuẩn bị key pair, CloudFormation template và Security Group</li>
              <li>Kết nối tới RDGW</li>
              <li>Triển khai Microsoft AD</li>
              <li>Thiết lập DNS</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>25/04/2026</td>
      <td>25/04/2026</td>
      <td><a href="https://000010.awsstudygroup.com/">https://000010.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>
            Tìm hiểu triển khai và bảo mật VPC Peering Connections
            <ul>
              <li>Cập nhật Network ACL</li>
              <li>VPC Peering</li>
              <li>Route Tables</li>
              <li>Cross-Peer DNS</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>26/04/2026</td>
      <td>26/04/2026</td>
      <td><a href="https://000002.awsstudygroup.com/">https://000002.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>

### THÀNH TỰU TUẦN 2: MẠNG NÂNG CAO & TRIỂN KHAI HẠ TẦNG

1. **Mạng AWS & kiến trúc VPC**
   - **Nền tảng VPC:** Thiết kế và triển khai thành công một Virtual Private Cloud (VPC) tuỳ chỉnh, bao gồm public/private subnets và Internet Gateways để kết nối ra bên ngoài.
   - **Điều hướng lưu lượng:** Cấu hình Route Tables và Security Groups để quản lý traffic vào/ra, đảm bảo kiểm soát bảo mật chi tiết theo từng instance.
   - **Giám sát:** Bật VPC Flow Logs để thu thập và phân tích thông tin IP traffic phục vụ troubleshooting và security auditing.

     ![w1_d5_1](/images/1-Worklog/w1_d5_1.png)
     ![w1_d5_2](/images/1-Worklog/w1_d5_2.png)
     ![w1_d5_3](/images/1-Worklog/w1_d5_3.png)
     ![w1_d5_4](/images/1-Worklog/w1_d5_4.png)

2. **EC2 Compute & giải pháp kết nối**
   - **Triển khai instance:** Khởi tạo và quản lý Amazon EC2 instances, xác minh kết nối qua VS Code và EC2 Instance Connect Endpoints.
   - **NAT (Network Address Translation):** Triển khai NAT Gateways để cho phép instances trong private subnets truy cập internet (cập nhật, tải gói...) trong khi vẫn tránh inbound traffic không mong muốn.
   - **Quan sát hệ thống:** Tích hợp CloudWatch Monitoring & Alerting để theo dõi hiệu năng và thiết lập cảnh báo tự động theo trạng thái hệ thống.

     ![w2_d2_1](/images/1-Worklog/w2_d2_1.png)
     ![w2_d2_2](/images/1-Worklog/w2_d2_2.png)
     ![w2_d2_3](/images/1-Worklog/w2_d2_3.png)

3. **Kết nối hybrid & đường hầm bảo mật**
   - **Site-to-Site VPN:** Xây dựng mô phỏng môi trường hybrid bằng cách thiết lập Site-to-Site VPN Connection.
   - **Định tuyến nâng cao:** Cấu hình VPN tunnels dùng Strongswan và Transit Gateway để tạo kênh kết nối an toàn, có khả năng mở rộng giữa mạng on-prem/remote và môi trường AWS.

4. **Dịch vụ định danh & thư mục (Microsoft AD)**
   - **Triển khai Directory:** Điều phối triển khai Microsoft Active Directory trên AWS bằng CloudFormation templates, tự động hoá hạ tầng theo hướng IaC.
   - **Quản trị từ xa:** Thiết lập truy cập quản trị an toàn qua Remote Desktop Gateway (RDGW) và cấu hình Private DNS để phân giải tên mượt mà trong domain.

5. **Kết nối liên VPC & bảo mật**
   - **VPC Peering:** Thiết lập thành công VPC Peering connections giữa nhiều VPC, cho phép chia sẻ tài nguyên private giữa các network segments.
   - **Phòng thủ mạng:** Tăng cường bảo mật bằng cách cập nhật Network ACLs (NACLs) và bật Cross-Peer DNS resolution để duy trì service discovery nhất quán giữa các VPC peered.