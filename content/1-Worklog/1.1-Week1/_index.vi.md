---
title: "Worklog Tuần 1"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Kết nối, làm quen với các thành viên trong First Cloud Journey.
* Nắm kiến thức AWS cơ bản và cách sử dụng AWS Console & AWS CLI.

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
          <li>Làm quen với các thành viên FCJ</li>
          <li>Đọc và ghi chú các nội quy, quy định tại đơn vị thực tập</li>
          <li>Tạo AWS Free Tier account</li>
          <li>Thiết lập MFA cho tài khoản</li>
        </ul>
      </td>
      <td>20/04/2026</td>
      <td>20/04/2026</td>
      <td></td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>Nhận đủ $200 Credit</li>
          <li>
            Tìm hiểu các dịch vụ AWS để nhận $100
            <ul>
              <li>EC2</li>
              <li>Amazon Bedrock</li>
              <li>Aurora &amp; RDS</li>
              <li>AWS Budgets</li>
              <li>AWS Lambda</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>21/04/2026</td>
      <td>21/04/2026</td>
      <td><a href="https://000001.awsstudygroup.com/3-chi%E1%BA%BFn-l%C6%B0%E1%BB%A3c-nh%E1%BA%ADn-%C4%91%E1%BB%A7-200-credit/">https://000001.awsstudygroup.com/3-chi%E1%BA%BFn-l%C6%B0%E1%BB%A3c-nh%E1%BA%ADn-%C4%91%E1%BB%A7-200-credit/</a></td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Tìm hiểu Cost Management với AWS Budgets
            <ul>
              <li>Tạo Budget</li>
              <li>Tạo Cost Budget</li>
              <li>Tạo Usage Budget</li>
              <li>Tạo RI Budget</li>
              <li>Tạo Savings Plans Budget</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>22/04/2026</td>
      <td>22/04/2026</td>
      <td><a href="https://000007.awsstudygroup.com/">https://000007.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Tìm hiểu AWS Support Plans
            <ul>
              <li>Truy cập AWS Support</li>
              <li>Quản lý yêu cầu hỗ trợ</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>23/04/2026</td>
      <td>23/04/2026</td>
      <td><a href="https://000009.awsstudygroup.com/">https://000009.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>
            Tìm hiểu IAM cơ bản
            <ul>
              <li>Tạo IAM Group và Users (Admin Group, Admin User, đăng nhập Admin User)</li>
              <li>Tạo IAM Role (Admin Role, OperatorUser)</li>
              <li>Switch Role</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>24/04/2026</td>
      <td>24/04/2026</td>
      <td><a href="https://000002.awsstudygroup.com/">https://000002.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>

### KẾT QUẢ TUẦN 1: NỀN TẢNG AWS & QUẢN LÝ CHI PHÍ

1. **Kiến thức nền tảng Cloud & Thiết lập ban đầu**
   - **Tài khoản & Bảo mật:** Khởi tạo thành công AWS Free Tier account và bật Multi-Factor Authentication (MFA) để bảo vệ tài khoản root.
   - **Tổng quan dịch vụ:** Nắm kiến thức nền tảng về các dịch vụ cốt lõi, bao gồm EC2, Amazon Bedrock, Aurora & RDS và AWS Lambda.

   ![w1_d2_1](/images/1-Worklog/w1_d2_1.png)

2. **Quản lý chi phí AWS & Lập ngân sách**
   - Làm chủ công cụ và chiến lược theo dõi/kiểm soát chi tiêu cloud với AWS Budgets:
     - **Tạo Budget & Cảnh báo:** Thiết lập các budget tuỳ chỉnh và cấu hình email cảnh báo tự động khi chi tiêu vượt ngưỡng.
     - **Theo dõi Cost & Usage:** Tạo Cost Budgets để theo dõi chi tiêu thực tế và Usage Budgets để theo dõi mức sử dụng tài nguyên theo dịch vụ.
     - **Lập kế hoạch tối ưu:** Tạo RI (Reserved Instance) Budgets và Savings Plans Budgets để theo dõi mức sử dụng và tối ưu hiệu quả chi phí.

   ![w1_d2_2](/images/1-Worklog/w1_d2_2.png)

3. **AWS Support & Quản lý Case**
   - Hiểu tổng quan hệ sinh thái AWS Support để xử lý các vấn đề kỹ thuật và billing:
     - **Support Plans:** So sánh các gói (Basic, Developer, Business, Enterprise) và cách chuyển đổi gói theo nhu cầu.
     - **Quản lý yêu cầu:** Thực hành tạo support case, chọn mức Severity phù hợp và trao đổi hiệu quả với kỹ sư hỗ trợ AWS.

   ![w1_d2_3](/images/1-Worklog/w1_d2_3.png)

4. **IAM cơ bản (Identity and Access Management)**
   - **Quản trị định danh:** Thiết lập cấu trúc quyền cơ bản bằng cách tạo IAM Groups và Admin Users phục vụ quản trị.
   - **Kiểm soát truy cập theo vai trò (RBAC):** Tạo IAM Roles (Admin, Operator) và sử dụng tính năng Switch Role để quản lý tài nguyên an toàn mà không cần dùng tài khoản root.

   ![w1_d2_4](/images/1-Worklog/w1_d2_4.png)


