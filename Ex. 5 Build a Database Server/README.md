<img width="1581" height="697" alt="image" src="https://github.com/user-attachments/assets/719c5085-18e0-49f4-87fa-27fd61cf6076" /># Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Imesha.S
* **Register Number**: 212225040131
* **Date of Submission**: 24/08/2026

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
First, I opened the AWS Management Console and went to the VPC service. I created a new security group named DB Security Group and configured it to allow MySQL (port 3306) access from the Web Security Group.

Next, I navigated to the RDS service and created a DB Subnet Group named DB-Subnet-Group. I selected the Lab VPC, chose two availability zones (us-east-1a and us-east-1b), and added the required subnets (10.0.1.0/24 and 10.0.3.0/24).

After that, I created a new Amazon RDS MySQL database instance. I selected Dev/Test template, enabled Multi-AZ deployment, and configured details like DB identifier (lab-db), username (main), and password (lab-password). I also selected db.t3.micro instance type and attached the DB Security Group.

Once the database was created, I waited until its status became available and then copied the endpoint URL from the connectivity section.

Finally, I opened the web application using the provided EC2 IP address, navigated to the RDS section, and entered the database details (endpoint, database name, username, password). After submitting, I successfully connected the app and tested it by adding and managing contacts in the address book.

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1535" height="707" alt="image" src="https://github.com/user-attachments/assets/cf0387c8-ff67-4cf7-8610-101ea5a2ab32" />


### Screenshot 2: Database Service Running

<img width="1612" height="707" alt="image" src="https://github.com/user-attachments/assets/42aa6c9d-99ea-4691-95a9-af9094b8618b" />

<img width="1581" height="697" alt="image" src="https://github.com/user-attachments/assets/4de1cd1f-a042-4c36-befd-2ceaef2eca22" />

### Screenshot 3: Sample Database and Table

<img width="1537" height="767" alt="image" src="https://github.com/user-attachments/assets/d7854340-beae-4a6f-a3a5-bb5594f3e94d" />


<img width="1477" height="701" alt="image" src="https://github.com/user-attachments/assets/bb5c0ac0-7b7a-42af-ab6e-7c8de13af3d3" />

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
