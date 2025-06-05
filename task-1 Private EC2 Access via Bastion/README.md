# Task 1: Establish connectivity to private EC2 instance from Public EC2 (Bastion Host)

Amazon EC2 (Elastic Compute Cloud) provides scalable virtual servers in the cloud. In secure deployments, private EC2 instances are not directly exposed to the internet. 

To access them securely, a **Bastion Host** (a public EC2 instance) is used. It acts as a gateway to connect to private instances within a **VPC (Virtual Private Cloud)** via SSH. 

This setup enhances security by limiting external access to only the bastion while allowing internal communication with private resources.


We put the Bastion Host in a public subnet that is linked to an Internet Gateway (IGW) in order to enable this configuration, which permits SSH access from your local computer. The target EC2 is located within a private subnet.

### 1) VPC Creation
![WhatsApp Image 2025-05-27 at 02 08 50_3694ac3a](https://github.com/user-attachments/assets/01d5f038-438c-4f8f-90cc-012012ab1c21)

### 2) Subnet Creation
![WhatsApp Image 2025-05-27 at 02 09 33_878756e4](https://github.com/user-attachments/assets/e9846039-e155-4511-8f35-be20198dbf94)

### 3) IGW creation
![WhatsApp Image 2025-05-27 at 02 11 42_9c00670f](https://github.com/user-attachments/assets/83cde9f9-5ecd-465a-9f5b-39a656bb8a6b)

### 4) IGW attached to VPC
![WhatsApp Image 2025-05-27 at 02 12 39_39e110a0](https://github.com/user-attachments/assets/8be3a579-dc50-4272-a73b-22c0f2d9ea77)

### 5) Updated subnet association for the Public route table
![WhatsApp Image 2025-05-27 at 02 26 18_bb75c7e8](https://github.com/user-attachments/assets/7b233faf-ff22-4b72-9a08-98d50aa2bcae)

### 6) SSH into the private subnet's ec2
![WhatsApp Image 2025-05-31 at 03 44 57_95301d7c](https://github.com/user-attachments/assets/0cbc57ce-80ef-44df-94d7-016678b58a82)
