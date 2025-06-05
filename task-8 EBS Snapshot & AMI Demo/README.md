# TASK-8 : Exploring EC2, EBS Snapshots & AMIs on AWS

This project demonstrates how to preserve and reuse EC2 instance data and configurations using EBS Snapshots and Amazon Machine Images (AMIs).

## Objective

To understand:
- How to take and restore EBS Snapshots
- How to create and launch AMIs
- The difference between storage-level (snapshot) and system-level (AMI) backups
- Data portability across different EC2 instances

## Steps Performed

### 1: Launch a Base EC2 Instance
![WhatsApp Image 2025-06-05 at 22 27 07_7922bb2f](https://github.com/user-attachments/assets/c72cde4a-f71a-4bdf-a558-229143778b86)
![WhatsApp Image 2025-06-05 at 22 32 51_5f058903](https://github.com/user-attachments/assets/214b9e60-d743-4e20-9fda-349f8acb91f5)

### 2: Connect and Add Data
![image](https://github.com/user-attachments/assets/cb576dd1-42a4-4a12-8004-4e30a6c604eb)

### 3: Create a Snapshot of the EBS Volume
![WhatsApp Image 2025-06-05 at 22 37 10_80d38dd0](https://github.com/user-attachments/assets/33153e4a-573b-4166-af14-dc7d930d5307)

### 4: Create a New EBS Volume from Snapshot
![WhatsApp Image 2025-06-05 at 22 48 42_0cc5caf2](https://github.com/user-attachments/assets/1bd5fef8-8fec-416d-bfd9-7ebf8ac22d5b)
![WhatsApp Image 2025-06-05 at 22 50 50_d52c6e89](https://github.com/user-attachments/assets/97e9b947-2b0e-4abb-84a6-203e291e8288)

### 5: Create an AMI from the Instance
![WhatsApp Image 2025-06-05 at 22 44 18_cd810fb1](https://github.com/user-attachments/assets/60c2a2f8-a7d0-4a6c-921a-684c7bc87ad1)

### 6: Launch a New EC2 Instance (RHEL)
![WhatsApp Image 2025-06-05 at 23 05 04_bacc410c](https://github.com/user-attachments/assets/47814531-b7f7-4a5f-819e-1797c21f7371)

### 7: Attach the Volume (from Snapshot)
![WhatsApp Image 2025-06-05 at 23 14 25_cb9bbe13](https://github.com/user-attachments/assets/a3231d3a-2f4e-435b-a681-f0add7b85274)
![WhatsApp Image 2025-06-05 at 23 16 50_0fa668e5](https://github.com/user-attachments/assets/4cd89cdf-6ccd-4599-a738-55248cbd7520)

### 8: Access Snapshot Data via Terminal
- Expected output: Hello from task8-instance-1!
![image](https://github.com/user-attachments/assets/0452f17b-a2c6-4f5c-8d0c-d40b711ba9ea)

### Testing AMI Portability
### 9: Launch a New EC2 Instance from AMI
![image](https://github.com/user-attachments/assets/52547c71-c7ef-4b9d-8a09-e2ab1a74129e)

### 10: Verify AMI-Based Instance
![image](https://github.com/user-attachments/assets/ff105d52-fbe4-41b8-a591-4801f6a77ea2)
