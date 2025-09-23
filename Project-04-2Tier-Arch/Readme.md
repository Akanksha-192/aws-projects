
# Project 04 – Secure Two-Tier Architecture on AWS Using a Bastion Host

## 🚀 Overview

In this project, we designed and implemented a secure two-tier architecture on AWS. A bastion host was deployed in a public subnet to provide secure SSH access to a private EC2 instance located in a private subnet. This ensures that the private instance remains isolated from the internet while still being accessible for administrative purposes through the bastion host.
This project is fully beginner-friendly and uses only AWS Free Tier services.

## 📌 Steps Implemented

#### Created VPC and Subnets
1. VPC: 10.0.0.0/16
2. Public Subnet: 10.0.1.0/24 (for Bastion Host)
3. Private Subnet: 10.0.2.0/24 (for Private EC2)
4. Attached Internet Gateway (IGW)
5. Connected IGW to the VPC.
6. Updated route table for Public Subnet → 0.0.0.0/0 via IGW.
#### Configured Security Groups
1. Bastion SG: Allowed SSH (port 22) only from My IP.
2. Private EC2 SG: Allowed SSH (port 22) only from Bastion SG.

#### Launched EC2 Instances
1. EC2 Bastion → Public Subnet, with Public IP.
2. EC2 Private → Private Subnet, without Public IP.

#### Verified Connectivity
1. SSH into Bastion Host from CloudShell.
2. From Bastion, SSH into the Private EC2 using its private IP.
3. Confirmed access worked securely.

## 🧹 Cleanup

To avoid ongoing costs:
1. Terminate both EC2 instances.
2. Delete Security Groups, Subnets, Route Tables, and Internet Gateway.
3. Finally, delete the VPC.

## 🎯 Skills Learned

- Amazon VPC (subnets, routing, IGW)
- Bastion Host concept and configuration
- Security Groups (restricted inbound rules)
- Private EC2 access patterns
- Secure multi-tier architecture on AWS

## Author
Project contribution by Akanksha, repo - *aws-projects*
