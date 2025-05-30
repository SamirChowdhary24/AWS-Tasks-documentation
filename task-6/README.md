# Task 6: VPC Examining Two AWS Accounts

For improved isolation, security, and management, resources are frequently dispersed across several AWS accounts in real-world cloud architectures. AWS has a powerful feature called *VPC Peering* that allows two *Virtual Private Clouds (VPCs)* to communicate with each other, even if they are part of different AWS accounts.

This task involves establishing *VPC Peering* between two VPCs, each of which is housed in a different AWS account. Creating VPCs, setting up subnets, connecting Internet Gateways (IGWs), and creating a *Peering Connection* that permits private communication between instances in one VPC and instances in the other are the steps involved.

To route traffic through the peering connection, *Route Tables* in both VPCs must be updated after the peering request is approved. In order to allow communication, *Security Groups* must also allow ICMP or other required protocols.

By avoiding the public internet and facilitating smooth networking between apps or services operating across various AWS accounts, this configuration improves *security* and *latency*. It is particularly helpful in shared services models between teams or organizational units, hybrid environments, and microservices architectures.


#### 1) VPC Creation
![WhatsApp Image 2025-05-30 at 22 01 38_a23b26db](https://github.com/user-attachments/assets/0bcfae52-1059-4b79-bb9a-466835887378)

#### 2) Route Tables Creation
![WhatsApp Image 2025-05-30 at 22 03 33_4119d77c](https://github.com/user-attachments/assets/3af45e1f-ae7f-429b-a6f7-0761807fb563)

#### 3) Subnet creation
![WhatsApp Image 2025-05-30 at 22 16 29_48a3c007](https://github.com/user-attachments/assets/9a5bf170-473d-449c-b6fb-d005a4608a8d)

#### 4) Edit Subnet associations
![WhatsApp Image 2025-05-30 at 22 18 21_2523397c](https://github.com/user-attachments/assets/b87e686a-53e5-47dc-bac7-0910c5098c32)
#### 5) Attach IGW to VPC
![WhatsApp Image 2025-05-30 at 22 23 28_c127298f](https://github.com/user-attachments/assets/a1e091c5-0c42-4239-881d-e0e32d33d8cb)
#### 6) Edit Route Table Routes
![WhatsApp Image 2025-05-30 at 22 28 19_a5d580b6](https://github.com/user-attachments/assets/c4f35412-5841-4924-86ff-56ebda79dba3)
#### 7) IGW
![WhatsApp Image 2025-05-30 at 22 31 55_2c64ff9d](https://github.com/user-attachments/assets/2f3d82a4-506e-47a2-bd71-9b5c766f943f)

#### 8) Instance Creation
![WhatsApp Image 2025-05-30 at 23 06 15_48449fc8](https://github.com/user-attachments/assets/3ff3717b-0822-4543-9fb5-2d24ed628cc4)

#### 9) VPC peering connection request
![WhatsApp Image 2025-05-30 at 23 14 15_61e2440d](https://github.com/user-attachments/assets/a7b2e7bb-edad-4f63-ad51-33e0603d18d5)

#### 10) VPC peering connection established
![WhatsApp Image 2025-05-30 at 23 14 32_0c0a6d68](https://github.com/user-attachments/assets/d335053a-d9dd-4550-98bb-301ab2c662ae)


#### 11) Access the other instance using SSH from the first instance and vice versa
![WhatsApp Image 2025-05-31 at 00 47 32_cdb7579e](https://github.com/user-attachments/assets/dbf627dc-0a08-4533-8a05-96d6f3f02040)

