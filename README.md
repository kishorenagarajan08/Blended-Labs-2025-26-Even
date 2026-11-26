# Blended-Labs
# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Kishore N
* **Register Number**: 212223230106
---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1. First, a security group named DB Security Group was created to allow the web server to connect to the database using port 3306 (MySQL).
2. A DB Subnet Group was created with subnets from two Availability Zones to allow the database to run in a Multi-AZ environment for high availability.
3. A MySQL RDS instance named lab-db was created with the database name lab, username main, and password lab-password.
4. The database was associated with the DB Security Group and the Lab VPC so that the web server can securely connect to the database.
5. The web application running on the EC2 server was opened using its IP address, and the RDS endpoint, database name, username, and password were entered to interact with the database.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server
<img width="1919" height="989" alt="Screenshot 2026-11-18 134740" src="https://github.com/user-attachments/assets/3ebd6ad3-04c9-4650-908c-6b901f8826bb" />



---

### Screenshot 2: Database Service Running
<img width="1919" height="992" alt="Screenshot 2026-11-18 135020" src="https://github.com/user-attachments/assets/a2a1964b-b05d-475e-8534-e7a912bed437" />



---

### Screenshot 3: Sample Database and Table

<img width="1919" height="991" alt="Screenshot 2026-11-18 140144" src="https://github.com/user-attachments/assets/dc511cb9-272d-4e51-8d42-45457b1155d2" />


---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst

# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
---
Name : Kishore N

Reg no : 212223230106

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)


1.Launched a new EC2 instance named Web Server in the N. Virginia region using Amazon Linux 2023 AMI and t2.micro instance type.

2.Enabled termination protection and stop protection, configured a security group, and added a user data script to install and start an Apache web server.

3.Monitored the instance using status checks, CloudWatch metrics, and system logs to ensure it was running properly.

4.Modified the security group to allow HTTP (port 80) traffic and accessed the web server using the public IP address.

5.Resized the instance to t2.small, increased the EBS volume size, explored EC2 service quotas, tested stop protection, and finally stopped the instance.


## Output Screenshots 

<img width="1919" height="864" alt="Screenshot 2026-11-25 135442" src="https://github.com/user-attachments/assets/f0141558-eb95-4fac-99fb-adf3d3d5727d" />
<img width="1919" height="870" alt="Screenshot 2026-11-25 135826" src="https://github.com/user-attachments/assets/40e35039-e836-495c-b124-87687fb3c849" />
<img width="1919" height="865" alt="Screenshot 2026-11-25 140120" src="https://github.com/user-attachments/assets/3392a5a1-37aa-46c0-abc1-5269a5a81683" />
<img width="1919" height="868" alt="Screenshot 2026-11-25 140419" src="https://github.com/user-attachments/assets/6fd102a7-1d04-434f-9e22-c50db3134490" />
<img width="1919" height="877" alt="Screenshot 2026-11-25 141110" src="https://github.com/user-attachments/assets/9d103a59-3b08-45db-927c-54d26caa003e" />
<img width="1916" height="868" alt="Screenshot 2026-11-25 144313" src="https://github.com/user-attachments/assets/abd5efd7-977b-4967-b9c0-b283094c316e" />




## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
