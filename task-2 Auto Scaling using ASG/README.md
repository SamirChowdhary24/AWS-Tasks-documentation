#  Task 2: Establish Auto Scaling using ASG

## Amazon EC2 and Auto Scaling

Amazon EC2 (Elastic Compute Cloud) allows you to run virtual machines in the cloud. However, managing these instances manually can become inefficient and time-consuming—especially when dealing with changing workloads. This is where **Auto Scaling** proves valuable, enabling your infrastructure to automatically adjust based on demand.

### Why Use Auto Scaling?

With **Auto Scaling Groups (ASG)**, you can ensure that the appropriate number of EC2 instances are running at all times based on predefined conditions such as:

- CPU utilization  
- Incoming traffic  
- Custom CloudWatch metrics

Auto Scaling maintains high availability and responsiveness by automatically **adding** or **removing** EC2 instances as needed.

---

### Key Steps to Set Up Auto Scaling

1. **Create an Amazon Machine Image (AMI)**  
   A snapshot of a configured EC2 instance that serves as a template to launch future instances.

2. **Define a Launch Configuration or Launch Template**  
   Specifies:  
   - Instance type  
   - AMI ID  
   - Key pair  
   - Security groups  
   - Other configurations

3. **Create an Auto Scaling Group (ASG)**  
   Configure the ASG to:  
   - Use the launch template/configuration  
   - Maintain a desired number of instances  
   - Scale in/out automatically

4. **Set Up CloudWatch Alarms**  
   Triggers that monitor metrics like CPU usage.  
   - If **CPU > 80%** → scale **out** (add instances)  
   - If **CPU < threshold** → scale **in** (terminate excess instances)

---

### Benefits

- Improved availability  
- Cost optimization  
- Hands-free resource management  
- Automatic response to load changes

Auto Scaling ensures your application remains available and efficient, even as demand fluctuates.

#### 1) AMI creation 
![WhatsApp Image 2025-05-27 at 01 52 41_5e2c2b4a](https://github.com/user-attachments/assets/2a9940d1-cbd8-4bfd-a9ec-70cf48f53d21)

#### 2) Asg Creation 
![WhatsApp Image 2025-05-27 at 01 51 16_178e5732](https://github.com/user-attachments/assets/87595d26-7a2c-40c8-bc58-40cbe92e8907)
