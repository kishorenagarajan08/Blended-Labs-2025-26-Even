# Blended-Labs

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
