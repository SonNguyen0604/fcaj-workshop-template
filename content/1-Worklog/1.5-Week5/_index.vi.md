---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Làm chủ kiến trúc & hiện đại hoá dữ liệu: từ di trú cơ sở dữ liệu đến triển khai Data Lake
* Kiến trúc NoSQL & phân tích dữ liệu nâng cao: đi sâu vào DynamoDB Design Patterns và xử lý dữ liệu serverless
* Di trú CSDL: cấu hình, giám sát và xử lý sự cố di trú dữ liệu bằng AWS DMS
* Data Lake trên AWS: xây dựng data pipelines qua S3 và Glue, phân tích với Athena và trực quan hoá bằng QuickSight
* DynamoDB nâng cao: triển khai các design patterns NoSQL nâng cao, ứng dụng serverless toàn cầu và kiến trúc event-driven
* Phân tích chi phí & hiệu năng: đo lường hiệu năng hệ thống và tối ưu chi phí hạ tầng với AWS Glue và Amazon Athena
* Data Engineering (DataBrew): dùng Cloud9 để upload datasets lên S3, dùng DataBrew để profiling, làm sạch và biến đổi dữ liệu

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
            Tìm hiểu chuyển đổi schema & di trú cơ sở dữ liệu
            <ul>
              <li>Chọn DMS source</li>
              <li>Chọn DMS target</li>
              <li>Serverless replication</li>
              <li>Giám sát DMS migrations</li>
              <li>Troubleshooting migrations với AWS DMS</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>18/05/2026</td>
      <td>18/05/2026</td>
      <td>
        <a href="https://000043.awsstudygroup.com/">https://000043.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Data Lake trên AWS
            <ul>
              <li>
                Thu thập và lưu trữ dữ liệu
                <ul>
                  <li>Tạo S3 Bucket</li>
                  <li>Tạo Delivery Stream</li>
                  <li>Tạo Sample Data</li>
                </ul>
              </li>
              <li>
                Tạo Data Catalog
                <ul>
                  <li>Tạo Glue Crawler</li>
                  <li>Kiểm tra dữ liệu</li>
                </ul>
              </li>
              <li>Biến đổi dữ liệu</li>
              <li>
                Phân tích và trực quan hoá
                <ul>
                  <li>Phân tích với Athena</li>
                  <li>Trực quan hoá với QuickSight</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </td>
      <td>19/05/2026</td>
      <td>19/05/2026</td>
      <td>
        <a href="https://000035.awsstudygroup.com/">https://000035.awsstudygroup.com/</a>
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        <ul>
          <li>
            Tìm hiểu LHOL: Hands-on Labs for Amazon DynamoDB
            <ul>
              <li>Khám phá DynamoDB</li>
              <li>Khám phá DynamoDB Console</li>
              <li>Sao lưu (backup)</li>
            </ul>
          </li>
          <li>Tìm hiểu LADV: Advanced Design Patterns for Amazon DynamoDB</li>
          <li>Tìm hiểu LMR: Build and Deploy a Global Serverless Application with Amazon DynamoDB</li>
          <li>Tìm hiểu LEDA: Build a Serverless Event Driven Architecture with DynamoDB</li>
        </ul>
      </td>
      <td>20/05/2026</td>
      <td>20/05/2026</td>
      <td><a href="https://000039.awsstudygroup.com/">https://000039.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        <ul>
          <li>
            Tìm hiểu phân tích chi phí & hiệu năng với AWS Glue và Amazon Athena
            <ul>
              <li>Chuẩn bị database</li>
              <li>Xây dựng database</li>
              <li>Kiểm tra database</li>
            </ul>
          </li>
          <li>
            Tìm hiểu phân tích chi phí và hiệu năng sử dụng
            <ul>
              <li>Dữ liệu trong bảng</li>
              <li>Chi phí</li>
              <li>Gắn tag và phân bổ chi phí</li>
              <li>Usage</li>
            </ul>
          </li>
        </ul>
      </td>
      <td>21/05/2026</td>
      <td>21/05/2026</td>
      <td><a href="https://000040.awsstudygroup.com/">https://000040.awsstudygroup.com/</a></td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        <ul>
          <li>Tạo Cloud9 Instance</li>
          <li>Tải dataset</li>
          <li>Upload dataset lên S3</li>
          <li>Thiết lập DataBrew</li>
          <li>Data Profiling</li>
          <li>Làm sạch & biến đổi dữ liệu</li>
        </ul>
      </td>
      <td>22/05/2026</td>
      <td>22/05/2026</td>
      <td><a href="https://000070.awsstudygroup.com/">https://000070.awsstudygroup.com/</a></td>
    </tr>
  </tbody>
</table>

### THÀNH TỰU TUẦN 5: HIỆN ĐẠI HOÁ DỮ LIỆU, KIẾN TRÚC DATA LAKE & NOSQL NÂNG CAO

1. **Chuyển đổi schema & di trú cơ sở dữ liệu**
   - **Triển khai AWS DMS:** Thiết kế pipeline di trú dữ liệu an toàn bằng cách thiết lập DMS sources và targets vững chắc.
   - **Replication & xử lý sự cố:** Vận hành serverless replication, cấu hình giám sát di trú theo thời gian thực và làm chủ kỹ thuật troubleshooting cho các đợt cutover CSDL phức tạp.

2. **Hạ tầng Enterprise Data Lake & phân tích dữ liệu**
   - **Thu thập & ingest dữ liệu:** Xây dựng ingestion pipelines có khả năng mở rộng, dùng Amazon S3 làm kho lưu trữ tập trung và Amazon Kinesis Delivery Streams.
   - **Catalog & trực quan hoá:** Điều phối tự động khám phá metadata với AWS Glue Crawlers và tích hợp Amazon Athena với Amazon QuickSight để phân tích serverless và BI.

3. **Kiến trúc NoSQL nâng cao & thiết kế event-driven**
   - **DynamoDB Design Patterns:** Đi sâu vào các pattern kiến trúc DynamoDB nâng cao (LHOL, LADV) để đạt scale lớn và tối ưu single-table design.
   - **Ứng dụng serverless toàn cầu:** Thiết kế ứng dụng phân tán toàn cầu, sẵn sàng cao (LMR) và triển khai workflow event-driven dạng serverless, decoupled (LEDA) dựa trên DynamoDB.

4. **FinOps & Data Engineering hiện đại**
   - **Tối ưu chi phí & hiệu năng:** Thực hiện phân tích chi tiết usage với AWS Glue và Athena, tận dụng tagging để phân bổ chi phí chính xác và nâng cao hiệu quả vận hành.
   - **Biến đổi dữ liệu (DataBrew):** Sử dụng môi trường AWS Cloud9 để điều phối workflow data engineering; triển khai AWS Glue DataBrew cho profiling, làm sạch và chuẩn bị dữ liệu tự động.


