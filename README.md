# Manual Dev Infra Setup for ScyllaDB

|**Author**        | **created on**       | **Version** |**Last edited on**| **Review Level**   | **Reviewer**      |
|---------------|------------|---------|--------|--------|----------------------|
| Pravalika Kanikarapu  | May 26  | v1.0|   May 27  | Pre-Reviewer   | Priyanshu            |
| Pravalika Kanikarapu  |  |  |   | L0             | Priyanka     |
| Pravalika Kanikarapu  |      |      |         | L1             | Rishabh Sharma       |
| Pravalika Kanikarapu  |      |      |         | L2             | Piyush Upadhyay      |

# Table of Contents

- [Introduction](#introduction)
- [Steps to Create Security Group for ScyllaDB](#Steps-to-Create-Security-Group-for-ScyllaDB)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)



# Introduction

This guide provides a step-by-step manual process for setting up a secure and functional development infrastructure for **ScyllaDB** on AWS. It includes detailed instructions on configuring a custom **Security Group**, which is essential to managing and protecting ScyllaDB access in your AWS environment. 


# Steps to Create Security Group for ScyllaDB

### 1. **Log in to AWS Management Console**

  
Go to the AWS Management Console.

### 2. **Navigate to the EC2 Dashboard**
- In the AWS Console, select **EC2** from the "Services" menu.

### 3. **Create a Security Group**
- In the left sidebar under **Network & Security**, click on **Security Groups**.
- Click the **"Create security group"** button.

  
![image](https://github.com/user-attachments/assets/51e5467e-d89c-4493-922a-6d2c3a019279)

### 4. **Configure Security Group Settings**

- **Name**: `SG-ScyllaDB`
- **Description**: `Security group for the ScyllaDB instance`
- **VPC**: Choose the correct VPC where your ScyllaDB instance will run.

![image](https://github.com/user-attachments/assets/e3bf2b6c-cdac-4376-9ba0-7d9457afd002)

![image](https://github.com/user-attachments/assets/23100396-bdba-4356-bc5d-8a5758eea5bf)

### 5. **Set Inbound Rules**

- Click on the Inbound rules tab.
- Click on Edit inbound rules.
- Add rules based on your requirements:
- Type: Custom TCP Rule
- Protocol: TCP
- Port Range: 9042 (for ScyllaDB) 22(for ssh)
- Source: Specify the security group of the employee app , salary app

![image](https://github.com/user-attachments/assets/c91b1b06-0bcd-4c87-9aaf-6291b994635c)

### 6. **Set Outbound Rules**

Click on the Outbound rules tab (defaults allow all traffic).
Optionally modify outbound rules as needed.

![image](https://github.com/user-attachments/assets/9ad63fd8-28c3-4515-b2b7-b37ead0ab72f)

# Conclusion

By completing this setup, you've successfully created a secure foundation for running **ScyllaDB** on AWS. This security group configuration ensures that only approved applications and users can access your ScyllaDB instances via CQL and SSH, helping you enforce access control and reduce risk in a production or development environment.The Security Group configuration for ScyllaDB is a critical part of securing your database infrastructure in AWS. 


#  Contact Information


| Name       | Email Address                |
|------------|------------------------------|
| Pravalika  | kanikarapu.pravalika.snaatak@mygurukulam.co|



#  Reference

| **Link**                                                                 | **Description**                                      |
|--------------------------------------------------------------------------|------------------------------------------------------|
| https://docs.scylladb.com/stable/architecture/security/ | Overview of security best practices and configurations for ScyllaDB.|
| https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html |Comprehensive guide to understanding and configuring AWS Security Groups |




