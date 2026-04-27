---
title: "Week 2 Worklog"
date: 2024-04-17
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---
### Week 2 Objectives:

* AWS Networking Fundamentals & Infrastructure Deployment
* Building Secure Cloud Infrastructure: From VPC Peering to Active Directory Integration

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
            Learn about Amazon VPC & Networking Fundamentals
            <ul>
              <li>Create VPC</li>
              <li>Create Subnet</li>
              <li>Create Internet Gateway</</li>
              <li>Create Route Table</li>
              <li>Create Security Group</li>
              <li>Enabale VPC Flow Logs</li>
            </ul>
          </li>
          </ul>
      </td>
      <td>22/04/2026</td>
      <td>22/04/2026</td>
      <td><a href="https://000003.awsstudygroup.com/3-prerequisite/">https://000003.awsstudygroup.com/3-prerequisite/</a></td>
      <td></td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        <ul>
          <li>
            Deploying Amazon EC2 Instances
            <ul>
              <li>Create EC2 Server</li>
              <li>Test connection with VS Code</li>
              <li>Create NAT Gateway</li>
              <li>Create EC2 Instance Connect Endpoint</li>
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
            Learn about Setting Up Site-to-site VPN Connection in AWS
            <ul>
              <li>Create a VPN Environment</li>
              <li>Configure VPN Connection</li>
              <li>VPN Connection using Strongswan with Transit Gateway</li>
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
            Learn about Deploying Microsoft Active Directory on AWS
            <ul>
              <li>Preparation key pair, CloudFormation template Security Group</li>
              <li>Connecting to RDGW</li>
              <li>Microsoft AD Deployment</li>
              <li>Set up DNS</li>
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
            Learn about Implementing and Securing VPC Peering Connections
            <ul>
              <li>Update Network ACL</li>
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


### WEEK 2 ACHIEVEMENTS: ADVANCED NETWORKING & INFRASTRUCTURE DEPLOYMENT

1. **AWS Networking & VPC Architecture**
   - **VPC Fundamentals:** Successfully designed and deployed a custom Virtual Private Cloud (VPC), including public/private subnets and Internet Gateways for external connectivity.
   - **Traffic Control:** Configured Route Tables and Security Groups to manage inbound and outbound traffic, ensuring granular security at the instance level.
   - **Monitoring:** Enabled VPC Flow Logs to capture and analyze IP traffic information for network troubleshooting and security auditing.
    ![w1_d2_2](/images/1-Worklog/w1_d5_1.png)
    ![w1_d2_2](/images/1-Worklog/w1_d5_2.png)
    ![w1_d2_2](/images/1-Worklog/w1_d5_3.png)
    ![w1_d2_2](/images/1-Worklog/w1_d5_4.png)
2. **EC2 Compute & Connectivity Solutions**
   - **Instance Deployment:** Launched and managed Amazon EC2 instances, verifying connectivity via VS Code and EC2 Instance Connect Endpoints.
   - **Network Address Translation:** Implemented NAT Gateways to allow instances in private subnets to securely access the internet for updates while remaining shielded from unsolicited inbound traffic.
   - **Observability:** Integrated CloudWatch Monitoring & Alerting to track instance performance and set up automated notifications for system health.
   ![w1_d2_2](/images/1-Worklog/w2_d2_1.png)
   ![w1_d2_2](/images/1-Worklog/w2_d2_2.png)
   ![w1_d2_2](/images/1-Worklog/w2_d2_3.png)

3. **Hybrid Connectivity & Secure Tunneling**
   - **Site-to-Site VPN:** Built a simulated hybrid environment by setting up a Site-to-Site VPN Connection.
   - **Advanced Routing:** Configured VPN tunnels using Strongswan and Transit Gateway to facilitate secure, scalable communication between remote networks and AWS environments.

4. **Identity & Directory Services (Microsoft AD)**
   - **Directory Deployment:** Orchestrated the deployment of Microsoft Active Directory on AWS using CloudFormation templates for automated infrastructure as code (IaC).
   - **Remote Management:** Established secure administrative access via Remote Desktop Gateway (RDGW) and configured Private DNS for seamless name resolution within the domain.

5. **Inter-VPC Connectivity & Security**
   - **VPC Peering:** Successfully established VPC Peering connections between multiple VPCs, allowing private resource sharing across different network segments.
   - **Network Defense:** Hardened network security by updating Network ACLs (NACLs) and enabling Cross-Peer DNS resolution to maintain consistent service discovery across peered networks.
