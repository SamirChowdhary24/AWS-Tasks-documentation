# Exploring AWS S3 via CLI — From Bucket Creation to Public Access

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

```bash
aws configure
