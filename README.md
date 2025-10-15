
# AWS Cloud Basics – EC2 and S3 Tasks

## Overview
This document provides a simple summary of two AWS beginner-level projects:
1. Creating and managing an EC2 instance.
2. Working with an S3 bucket for file storage, versioning, and secure access.

---

## Task 1: AWS EC2 Instance File Management

### Aim
To learn how to launch an EC2 instance, connect to it using SSH, create files and folders, compress them into a zip file, and then extract them back.

### Steps
1. Log in to AWS Management Console and go to **EC2**.
2. Launch a new instance using **Amazon Linux 2 / Ubuntu AMI**.
3. Choose **t2.micro (Free Tier)** and create or select a key pair.
4. Configure the security group to allow **SSH (port 22)**.
5. Launch and connect to the instance using the command:
   ```bash
   ssh -i "devops.pem" ec2-user@<public-ip>
   ```
6. Inside the instance, create a folder and files:
   
   ```bash
   mkdir myproject
   cd myproject
   echo "File 1 content" > file1.txt
   echo "File 2 content" > file2.txt
   echo "File 3 content" > file3.txt
   ```
7. Zip the files and then unzip them:
   ```bash
   zip myfiles.zip file1.txt file2.txt file3.txt
   unzip myfiles.zip
   ```

### Result
You have successfully created and managed files on an EC2 instance using basic Linux commands.

---

## Task 2: AWS S3 Bucket Management

### Aim
To create and manage an S3 bucket, upload files, enable versioning, and generate a pre-signed URL for secure access.

### Steps
1. Open the **AWS Management Console → S3**.
2. Click **Create Bucket**, give it a unique name, and choose a region (e.g., Asia Pacific - Mumbai).
3. Keep **Block Public Access** enabled and create the bucket.
4. Open the bucket and upload some files (e.g.,image1.jpg).
5. Enable **Bucket Versioning** under the **Properties** tab.
6. Re-upload a file to create a new version.
7. Generate a **Pre-signed URL** using AWS CLI:
   ```bash
   aws s3 presign s3://devopsproject.1/71405-1920x1080-desktop-1080p-red-dead-redemption-wallpaper-image.jpg
   ```

🔗 **S3 Bucket Link:** [View My Bucket](https://s3.eu-north-1.amazonaws.com/devopsproject.1/71405-1920x1080-desktop-1080p-red-dead-redemption-wallpaper-image.jpg)


### Result
An S3 bucket was successfully created, versioning was enabled, and files can now be securely accessed using a temporary pre-signed URL.

---

## Learnings
- Gained practical understanding of **AWS EC2** and **S3**.
- Learned basic **Linux file operations** on a cloud instance.
- Understood **cloud storage management**, **version control**, and **secure file sharing**.
- Built a foundation for working with more advanced AWS services.

---

## Author
**Name:** Keerthivasan.B
**Course:** MCA – MCET College  

---
