# Project 05 – VPC Peering Between Mumbai & Hyderabad

## 🚀 Overview
In this project, we established **cross-region connectivity** by setting up **VPC Peering** between Mumbai (ap-south-1) and Hyderabad (ap-south-2).
This setup allows private communication between resources in different regions while staying entirely within the AWS Free Tier.

---

## 📌 Steps Implemented
**1. Created VPCs and Subnets -**
Mumbai VPC → 10.0.0.0/16 with subnet 10.0.1.0/24
Hyderabad VPC → 10.1.0.0/16 with subnet 10.1.1.0/24

**2. Created Internet Gateways ( IGW )-**
Attached IGWs to both VPCs.
Updated route tables with explicit subnet associations.

**3. Configured Security Groups -**
Allowed SSH (port 22) from personal IP for admin access.
Allowed ICMP (ping) for testing connectivity.

**4. Launched EC2 Instances -**
One instance in each VPC (Mumbai & Hyderabad).
Used key pairs for secure SSH access.

**5. Established VPC Peering -**
Created a peering connection (Requester = Mumbai, Accepter = Hyderabad).
Accepted the request from Hyderabad VPC.
Updated route tables in both VPCs to send traffic through the peering connection.

**6. Verified Connectivity -**
Connected to EC2 instances using AWS CloudShell + SSH.
Successfully pinged private IPs across regions via the peering link.

---

## 🧹 Cleanup
To avoid unnecessary resource usage:

1. Terminate EC2 Instances in both regions.
2. Delete VPC Peering Connection.
3. Detach & Delete IGWs.
4. Delete VPCs and Subnets.

---

### Project Contribution By Akanksha under *aws-projects* repository
