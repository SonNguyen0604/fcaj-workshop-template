---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Week 7 Objectives:

* Deploy Application on Docker: Deep dive into multi-container containerization, local deployment, and AWS cloud architecture integration.
* Container Management & Deployment: Build, manage, and deploy software applications using Docker containers, Docker Compose, and Amazon EC2 instances.
* Image Registries & Database Integration: Create and configure container repositories on Amazon ECR and Docker Hub, and connect application containers with Amazon RDS (MySQL) within isolated VPC security groups.


### Tasks to be carried out this week:
<table>
  <thead>
    <tr>
      <th>Day</th>
      <th>Task</th>
      <th>Start Date</th>
      <th>Completion Date</th>
      <th>Reference Material</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2</td>
      <td>
      <ul>
        <li>
            Deploy on Local
            <ul>
              <li>Install Dependencies</li>
              <li>Deploy Application</li>
              <li>Test Application</li>
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
            Preparation & Infrastructure Setup
            <ul>
                <li>Preparation steps for AWS deployment</li>
                <li>Launch RDS Instance</li>
                <li>Configuring EC2 Instance</li>
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
            Deploy use only Docker Image
            <ul>
              <li>6.1. Deploy Application (Nginx, Application, Webserver)</li>
              <li>6.2. Test Application connected to Amazon RDS (MySQL)</li>
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
            Deploy with Docker Compose
              <ul>
                <li>7.1. Deploying the Application using Docker Compose & Docker Daemon</li>
                <li>7.2. Testing the multi-container Application stack</li>
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
            Push Image & Clean Up
               <ul>
                <li>8.1. Using ECR (Create Elastic Container Registry for Frontend Image)</li>
                <li>8.2. Use Docker Hub</li>
                <li>9. Clean Up Resources</li>
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


### WEEK 7 ACHIEVEMENTS: DEPLOY APPLICATION ON DOCKER WORKSHOP

1. **Local Containerization & Application Testing**
   - **Environment Isolation:** Evaluated the benefits of containerized baselines over personal local host systems using Docker platform environments.
   - **Stack Verification:** Successfully containerized and validated a multi-tier application stack consisting of a Browser client, Nginx Server, Web Applications (React/Node.js), and Database Engines.

2. **Cloud Architecture & Container Hosting Pipeline**
   - **Compute & Database Provisioning:** Configured Amazon EC2 hosting nodes and deployed an Amazon RDS (MySQL) database engine isolated within a private subnet group.
   - **Network Security Segregation:** Orchestrated traffic flow through an AWS VPC Internet Gateway, implementing isolated Security Groups for Public EC2 instance contents and Private DB SG layers.

3. **Multi-Container Orchestration & Registry Management**
   - **Docker Compose Implementation:** Streamlined application services orchestration by managing container groups directly via the Docker Daemon and Docker Compose configurations.
   - **Image Management & Hosting:** Engineered and established artifact deployment pathways by pushing verified container images to remote public/private registries, including Amazon Elastic Container Registry (ECR) and Docker Hub.