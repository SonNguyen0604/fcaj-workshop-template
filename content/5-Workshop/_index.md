*Nhấn **Commit changes...** để lưu lại file Tiếng Việt.*

---

### Bước 3: Cập nhật bản Tiếng Anh (`_index.md`)
Bây giờ ông mở file tiếng Anh **`_index.md`** ngay trong thư mục đó, chọn biểu tượng cây bút chì (`✏️`) và dán toàn bộ đoạn mã tiếng Anh kỹ thuật chuẩn hóa này vào:

```markdown
---
title: "Building High Availability Systems"
date: 2026-06-22
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# WORKSHOP: ENSURING HIGH AVAILABILITY ON AWS

This comprehensive workshop guides you through the process of designing, deploying, and operating a fault-tolerant and auto-scaling infrastructure on AWS for a Python web application.

---

### 1. Overview & Architecture Diagram

The infrastructure is engineered following the AWS Well-Architected Framework (Reliability Pillar) guidelines, ensuring the application remains operational 24/7 even during a total Availability Zone failure.

* **Architecture Diagram:**
  
  `[Member 2: Insert the system architecture diagram designed via Draw.io/Excalidraw here]`

* **AWS Services Utilized:** Amazon VPC, Application Load Balancer (ALB), Auto Scaling Group (ASG), Amazon EC2, Amazon RDS Multi-AZ, Amazon S3, Amazon CloudWatch.

---

### 2. Prerequisites

To execute this technical lab successfully, you need:
* An AWS Account provisioned with administrative privileges (IAM AdministratorAccess).
* AWS CLI and Docker Desktop configured on your local workstation.
* The source code for the Python demo application.

---

### 3. Step-by-Step Guide

#### **Step 1: Provisioning a Multi-AZ VPC Network Infrastructure**
* **Details:** Configure an AWS VPC spanning two isolated Availability Zones (AZ-A and AZ-B). Each AZ is divided into a Public Subnet (routed to the Internet Gateway) and a Private Subnet.
* **Console Screenshots:**
  
  `[Member 2: Insert VPC, Subnets, and Route Tables console screenshots here]`

#### **Step 2: Deploying a Multi-AZ Amazon RDS Database Engine**
* **Details:** Launch an Amazon RDS Database Instance within the Private Subnet Subnet Group, enabling Multi-AZ deployment for real-time synchronous standby replication.
* **Console Screenshots:**
  
  `[Member 2: Insert RDS Multi-AZ operational status screenshots here]`

#### **Step 3: Containerizing and Deploying the Python Application on EC2**
* **Details:** Write a Dockerfile to containerize the Python app, build the image, and deploy it onto an EC2 Instance to test connectivity with RDS and S3 resources.
* **Configuration Snippet:**
  ```dockerfile
  # Dockerfile template or application connection strings
  # [Member 3: Insert the Dockerfile/Python DB connection code block here]
