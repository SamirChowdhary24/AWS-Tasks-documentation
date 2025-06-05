
# Task 4: Hosting a Domain Using Route 53 with ALB-Based Routing

This documentation outlines the step-by-step process of hosting a domain using Amazon Route 53 and configuring path-based and host header-based routing using an Application Load Balancer (ALB) in AWS. The objective of this setup is to route incoming traffic to different backend services based on URL paths or domain headers while ensuring secure HTTPS communication.

---

## Domain Configuration (Routing Side)

1. **Purchase a Domain**  
   Buy a domain from any registrar such as GoDaddy, Namecheap, or Hostinger.

2. **Create a Hosted Zone in Route 53**  
   - Go to the AWS Route 53 dashboard.  
   - Create a public hosted zone for your purchased domain (e.g., `example.com`).  
   - AWS will generate NS (Name Server) records.

3. **Update Name Servers in Domain Registrar**  
   - Copy the NS records from the Route 53 hosted zone.  
   - Log in to your domain registrar's dashboard.  
   - Replace the default NS records with the ones provided by Route 53 to point your domain to AWS.

4. **Request an SSL Certificate using ACM (AWS Certificate Manager)**  
   - Navigate to the AWS Certificate Manager (ACM).  
   - Request a public certificate for both `example.com` and `*.example.com`.  
   - Choose DNS validation and copy the CNAME record provided by ACM.

5. **Validate the Certificate**  
   - Go back to your Route 53 hosted zone.  
   - Add the CNAME record (provided by ACM) to validate domain ownership.  
   - Wait for ACM to issue the certificate.

---

## Application Setup (Application Side)

1. **Launch EC2 Instances**  
   - Deploy EC2 instances in the same VPC where ALB will be configured.  
   - Install and configure a web server (e.g., Nginx or Apache).  
   - Ensure each EC2 instance listens on specific ports (e.g., 80, 7764, or 9097) as per your application's structure.

2. **Create Target Groups**  
   - Go to the EC2 dashboard → Target Groups.  
   - Create separate target groups for each service.  
   - Register corresponding EC2 instances in each target group, specifying the correct port.  
   - Configure health check paths appropriately.

---

## ALB Configuration (Rules Side)

1. **Create an Application Load Balancer**  
   - Go to the EC2 dashboard → Load Balancers → Create Load Balancer.  
   - Choose **Application Load Balancer** (ALB).  
   - Select **Internet-facing** and choose at least two Availability Zones.  
   - Select the same VPC where your EC2 instances and target groups are configured.  
   - Assign a security group that allows inbound traffic on **HTTP (80)** and **HTTPS (443)**.

2. **Configure Listeners and Rules**

   **HTTP Listener (Port 80):**
   - Add a listener for port 80.
   - Set a default action to forward traffic to one of the target groups.
   - Create a rule to **redirect all HTTP traffic to HTTPS** for secure communication.

   **HTTPS Listener (Port 443):**
   - Add a listener for port 443.
   - Attach the SSL certificate obtained from ACM.
   - Define routing rules:
     - **Path-based routing:** Forward requests based on specific URL paths (e.g., `/api`, `/admin`) to different target groups.
     - **Host header-based routing:** Forward traffic based on the `Host` value (e.g., `api.example.com`, `admin.example.com`).

---

## Route 53 DNS Configuration

1. **Create an A Record with Alias**  
   - In your Route 53 hosted zone, create a new **A Record**.  
   - Set the record type to **Alias**.  
   - For the alias target, select the DNS name of your Application Load Balancer.  
   - Save the record to complete domain mapping.

2. **Domain Routing**  
   This setup ensures that:
   - Your custom domain routes to the Application Load Balancer.
   - ALB listens for HTTP/HTTPS traffic and forwards it securely.
   - Routing is controlled via defined path-based and host header-based rules.

---

## Summary

With this configuration, incoming traffic to your domain is securely routed via HTTPS to specific backend services based on request paths or host headers. This setup improves scalability, security, and modular management of different application components using AWS-managed infrastructure.


