DecodeLabs - AWS EC2 Static Website

📌 Project Overview

This project demonstrates the deployment of a static website on an
Amazon EC2 instance using Amazon Linux and Nginx.

The objective was to understand the basic workflow of deploying and
accessing a web server in the AWS Cloud.



🏗️ Architecture

Internet
   |
   | HTTP :80
   v
AWS Security Group
   |
   v
Amazon EC2
   |
   v
Amazon Linux
   |
   v
Nginx
   |
   v
Static HTML Website

---
 ☁️ AWS Services Used

- Amazon EC2
- EC2 Key Pair
- Security Groups

---

💻 Technologies Used

- Amazon Linux
- Linux
- Nginx
- HTML
- CSS
- SSH
- GitHub

---

🔐 Security Group Configuration

Inbound Rules

| Protocol | Port | Source | Purpose |
|---|---:|---|---|
| TCP | 22 | My IP (/32) | SSH administration |
| TCP | 80 | 0.0.0.0/0 | Public HTTP access |

### Outbound Rules

| Protocol | Port | Destination |
|---|---:|---|
| All traffic | All | 0.0.0.0/0 |

SSH access was restricted to my IP address instead of allowing
SSH access from the entire internet.

---

 🚀 Deployment Process

1. Launch EC2 Instance

Created an EC2 instance running Amazon Linux.

2. Configure SSH Access

Created an EC2 key pair and used the private key to securely connect
to the instance through SSH.
 3. Connect to Amazon Linux

Connected to the EC2 instance using:

bash
ssh -i <private-key> ec2-user@<public-ip>
