---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Làm chủ hiệu quả vận hành AWS: từ giám sát CloudWatch đến tự động hoá bằng CLI
* Tối ưu tầng dữ liệu: xây dựng NoSQL có khả năng mở rộng & giải pháp caching hiệu năng cao

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
            Tìm hiểu Amazon CloudWatch
            <ul>
              <li>CloudWatch Metrics</li>
              <li>CloudWatch Logs</li>
              <li>CloudWatch Alarms</li>
              <li>CloudWatch Dashboards</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>11/05/2026</td>
      <td>11/05/2026</td>
      <td>
        <a href="https://000008.awsstudygroup.com/">https://000008.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Quản lý DNS Hybrid với Amazon Route 53
            <ul>
              <li>Kết nối tới RDGW</li>
              <li>Triển khai Microsoft AD</li>
              <li>
                Thiết lập DNS
                <ul>
                  <li>Tạo Route 53 Outbound Endpoint</li>
                  <li>Tạo Route 53 Resolver Rules</li>
                  <li>Tạo Route 53 Inbound Endpoints</li>
                  <li>Kiểm thử kết quả</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </td>
      <td>12/05/2026</td>
      <td>12/05/2026</td>
      <td>
        <a href="https://000010.awsstudygroup.com/">https://000010.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Thao tác dòng lệnh với AWS CLI
            <ul>
              <li>Cài đặt AWS CLI</li>
              <li>Xem tài nguyên qua CLI</li>
              <li>AWS CLI với Amazon S3</li>
              <li>AWS CLI với Amazon SNS</li>
              <li>AWS CLI với IAM</li>
              <li>AWS CLI với VPC</li>
              <li>Tạo EC2 bằng AWS CLI</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>13/05/2026</td>
      <td>13/05/2026</td>
      <td><a href="https://000011.awsstudygroup.com/">https://000011.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Amazon DynamoDB
            <ul>
              <li>
                Bắt đầu với Python và DynamoDB
                <ul>
                  <li>Tạo bảng</li>
                  <li>Ghi dữ liệu</li>
                  <li>Đọc dữ liệu</li>
                  <li>Cập nhật dữ liệu</li>
                  <li>Xoá dữ liệu</li>
                  <li>Nạp dữ liệu mẫu</li>
                  <li>Truy vấn dữ liệu</li>
                  <li>Scan dữ liệu</li>
                  <li>Xoá bảng</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </td>
      <td>14/05/2026</td>
      <td>14/05/2026</td>
      <td><a href="https://000060.awsstudygroup.com/">https://000060.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Amazon ElastiCache
            <ul>
              <li>
                Tạo ElastiCache cluster
                <ul>
                  <li>Tạo cluster (cluster mode disabled)</li>
                  <li>Tạo cluster (cluster mode enabled)</li>
                  <li>Cấp quyền truy cập tới cluster</li>
                  <li>Kết nối tới cluster node</li>
                </ul>
              </li>
              <li>
                Dùng AWS SDK để ghi/đọc dữ liệu trên ElastiCache
                <ul>
                  <li>Tạo ElastiCache cluster</li>
                  <li>Kết nối tới ElastiCache</li>
                  <li>Set và Get strings</li>
                  <li>Publish (write) và subscribe (read)</li>
                  <li>Set và Get hash với nhiều items</li>
                  <li>Ghi và đọc từ stream</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </td>
      <td>15/05/2026</td>
      <td>15/05/2026</td>
      <td><a href="https://000045.awsstudygroup.com/">https://000045.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>

### THÀNH TỰU TUẦN 4: GIÁM SÁT CLOUD, TỰ ĐỘNG HOÁ & KIẾN TRÚC DỮ LIỆU NÂNG CAO

1. **Giám sát hạ tầng & khả năng quan sát**
   - **Amazon CloudWatch:** Thiết lập hệ thống giám sát toàn diện với CloudWatch Metrics và Logs để theo dõi sức khoẻ hệ thống.
   - **Quản trị chủ động:** Cấu hình CloudWatch Alarms và Dashboards tương tác để tự động cảnh báo và trực quan hoá hiệu năng tài nguyên theo thời gian thực.

2. **Mạng nâng cao & kết nối hybrid**
   - **Quản lý DNS Hybrid:** Triển khai kiến trúc DNS phức tạp với Amazon Route 53, bao gồm Inbound/Outbound Endpoints và Resolver Rules.
   - **Tích hợp hạ tầng:** Quản lý kết nối liền mạch giữa môi trường Microsoft AD và tài nguyên cloud thông qua RD Gateway.

3. **Tự động hoá DevOps & làm chủ CLI**
   - **Thành thạo AWS CLI:** Tối ưu quản trị hạ tầng bằng các thao tác dòng lệnh, gồm tự động hoá provisioning tài nguyên cho S3, SNS và IAM.
   - **Triển khai bằng lệnh:** Làm chủ việc tạo và quản lý EC2 instances cùng cấu hình VPC trực tiếp qua terminal để nâng cao hiệu quả workflow.

4. **Giải pháp dữ liệu hiệu năng cao & caching**
   - **NoSQL (DynamoDB):** Thiết kế data model có khả năng mở rộng với Amazon DynamoDB; thực hành CRUD, truy vấn nâng cao và indexing, tích hợp với Python.
   - **Tăng tốc in-memory:** Triển khai Amazon ElastiCache clusters để giảm độ trễ ứng dụng; sử dụng AWS SDK cho cấu trúc dữ liệu phức tạp và stream processing.