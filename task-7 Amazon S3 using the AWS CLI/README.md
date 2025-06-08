# Task-7 : Exploring AWS S3 via CLI — From Bucket Creation to Public Access

This repository documents my hands-on experience using the AWS CLI to interact with Amazon S3. The goal was to create a new S3 bucket, upload a file, configure public access, and retrieve the file via its public URL — all through the command line following AWS best practices.

---

## Tools & Technologies

- AWS CLI (v2)
- Git Bash (on Windows)
- Amazon S3
- IAM credentials

---

## Objectives

- Create an S3 bucket in a specified region
- Upload a file using AWS CLI
- Make the object publicly accessible
- Access the file from a browser via public URL
- Understand S3 permissions: ACLs vs. Bucket Policies

---

## Steps Followed

### 1. Configure AWS CLI
![WhatsApp Image 2025-06-05 at 17 41 00_18e40d71](https://github.com/user-attachments/assets/903be1a5-b07b-47d1-82d9-14b3c43987f0)

### 2. Create an S3 Bucket
![WhatsApp Image 2025-06-05 at 18 11 17_50b0c434](https://github.com/user-attachments/assets/90242263-4dd1-4ebb-b4c7-c268b74cd889)
![WhatsApp Image 2025-06-05 at 18 12 13_7cdcb0ca](https://github.com/user-attachments/assets/3201fffc-9855-4111-b199-bcd17877e238)

### 3.  Disable Public Access Block
By default, AWS S3 blocks all public access to protect your data from being accidentally exposed. This is called the Public Access Block feature, which acts as a safety net.
When you want to make certain files or buckets publicly accessible (for example, to share a website or allow public downloads), you need to disable the Public Access Block settings first. This unlocks the possibility for public access.
![WhatsApp Image 2025-06-05 at 18 30 05_ba1c5797](https://github.com/user-attachments/assets/e17ada4a-d78e-429b-a56f-4b9582278d93)

### 4. Upload a File to the Bucket
![WhatsApp Image 2025-06-05 at 18 37 25_cd914e80](https://github.com/user-attachments/assets/c42b49d4-2ca1-478c-9214-473486865fa0)
![WhatsApp Image 2025-06-05 at 18 38 19_29ba0548](https://github.com/user-attachments/assets/94e1c560-0646-440d-ab0e-27702c5e0b45)

### 5. Set Bucket Policy to Allow Public Access
![WhatsApp Image 2025-06-05 at 18 51 31_a922117f](https://github.com/user-attachments/assets/cb04189d-3704-466f-8e1e-1513e5eeda9f)

### 6. Access the File via Browser
![WhatsApp Image 2025-06-05 at 18 52 23_4b3b92d8](https://github.com/user-attachments/assets/3dd28f5e-6bd3-4455-9cb5-fc0f7485152f)


