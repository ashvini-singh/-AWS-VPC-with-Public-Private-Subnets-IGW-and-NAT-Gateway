# 🌐 AWS VPC with Public & Private Subnets, IGW, and NAT Gateway

This project provides a **fully functional AWS VPC setup** using the AWS Console (no CLI required). It includes public and private subnets, an internet gateway, a NAT gateway, and the proper route tables for secure internet access and traffic isolation.

---

## 📐 Architecture Diagram

![image](https://github.com/user-attachments/assets/f0569055-0bff-4f6c-a05f-8fb15239d3d6)

---

## 🚀 What’s Inside

- ✅ **1 VPC** with CIDR block `172.20.0.0/16`
- ✅ **2 Public Subnets** across AZs (`ap-south-1a`, `ap-south-1b`)
- ✅ **2 Private Subnets** across AZs
- ✅ **Internet Gateway (IGW)** for public subnets
- ✅ **NAT Gateway** for secure internet from private subnets
- ✅ **Route Tables** with correct routing configuration

---

## 🧱 Subnet Breakdown

| Subnet Name            | CIDR Block      | AZ           | Type     |
|------------------------|------------------|--------------|----------|
| subnet-public-1        | 172.20.1.0/24     | ap-south-1a  | Public   |
| subnet-public-2        | 172.20.2.0/24     | ap-south-1b  | Public   |
| subnet-private-1       | 172.20.10.0/24    | ap-south-1a  | Private  |
| subnet-private-2       | 172.20.11.0/24    | ap-south-1b  | Private  |

---

## 🛠️ Step-by-Step Guide (AWS Console)

1. **Create VPC**  
   - CIDR block: `172.20.0.0/16`  
   - Name: `my-vpc`

2. **Create Subnets**  
   - 2 public, 2 private in different AZs  
   - Enable auto-assign public IP for public subnets

3. **Attach Internet Gateway (IGW)**  
   - Name: `my-igw`  
   - Attach to your VPC

4. **Create NAT Gateway**  
   - In public subnet  
   - Allocate Elastic IP

5. **Route Tables**  
   - Public RT: route `0.0.0.0/0` → IGW  
   - Private RT: route `0.0.0.0/0` → NAT Gateway

---

## 📗 Related Blog

Check out the full tutorial on [Medium](https://ashwini-singh.medium.com/create-a-secure-vpc-on-aws-with-public-private-subnets-igw-nat-gateway-no-cli-ed1c3533618a) 

---
                                            
## 🔐 Security Notes

- Keep backend services (like databases) in private subnets  
- Use Security Groups and NACLs to control access  
- Monitor traffic with VPC Flow Logs

---

## 🧾 License

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-blue.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

This project is licensed under [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).

---

## 🧠 Author

Made with 💻 by (https://github.com/ashvini-singh)  
Feel free to fork, share, or suggest improvements!

