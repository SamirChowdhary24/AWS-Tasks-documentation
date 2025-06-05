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
![WhatsApp Image 2025-06-05 at 22 31 06_ab7bd93e](https://github.com/user-attachments/assets/40be63a5-c07d-4bb7-b949-18b913f52db3)

### 3: Create a Snapshot of the EBS Volume
![WhatsApp Image 2025-06-05 at 22 37 10_80d38dd0](https://github.com/user-attachments/assets/33153e4a-573b-4166-af14-dc7d930d5307)

### 4: Create a New EBS Volume from Snapshot
![WhatsApp Image 2025-06-05 at 22 48 42_0cc5caf2](https://github.com/user-attachments/assets/1bd5fef8-8fec-416d-bfd9-7ebf8ac22d5b)
![WhatsApp Image 2025-06-05 at 22 50 50_d52c6e89](https://github.com/user-attachments/assets/97e9b947-2b0e-4abb-84a6-203e291e8288)

### 5: Create an AMI from the Instance
![WhatsApp Image 2025-06-05 at 22 44 18_cd810fb1](https://github.com/user-attachments/assets/60c2a2f8-a7d0-4a6c-921a-684c7bc87ad1)

### 6: Launch a New EC2 Instance (RHEL)


