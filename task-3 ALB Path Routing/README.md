# Task 3: Application Load Balancer-Based Path-Based Routing

The *Application Load Balancer (ALB)* is one of the strong traffic management tools offered by *Amazon Web Services (AWS). Using request attributes like URL path, host headers, or query strings, ALB is made to route HTTP and HTTPS traffic to your targets. One of the most popular methods is **Path-Based Routing*, which routes traffic to various target groups according to the URL path in incoming requests.

For instance, the ALB can use these paths to route traffic to various backend resources (such as EC2 instances) if you have multiple applications running in different environments (e.g., /app1 and /app2).

Creating a *Application Load Balancer* and establishing listener rules to analyze the path in the incoming requests are the first steps in setting this up. Depending on the specified path, the listener will forward traffic to various *Target Groups* (traffic to /app1/* goes to Target Group 1 and /app2/* goes to Target Group 2). One or more EC2 instances or additional resources, such as Lambda functions, may be present in each target group.

Additionally, you set up *Nginx* (or another server) on the backend to manage the traffic and route it according to the URL path. For instance, the ALB may handle requests to /app1 behind the scenes, while another application may handle requests to /app2. These Apps will be hosted on two different instances.

With *Path-Based Routing*, you can maintain a tidy and effective infrastructure configuration while optimizing traffic flow, isolating application tiers, and enhancing scalability by allocating traffic to various resources according to the URL path.

#### 1) ALB 
![WhatsApp Image 2025-05-31 at 02 53 59_8bf464a2](https://github.com/user-attachments/assets/03796ebd-3035-461f-b1ae-216dba2a923b)


#### 2) Two target groups for each instance
![image](https://github.com/user-attachments/assets/2dac9cb6-77e6-4957-8b77-b9450eec93d6)


#### 3) Health Checks for both of the target groups 
![image](https://github.com/user-attachments/assets/7906bfaa-d309-41a9-9bcf-09e50781e2d3)
![image](https://github.com/user-attachments/assets/261a31b8-ddcd-4044-b96a-a4e1fee283c0)


#### 4) Final result, the index.html page after alb routes the traffic to the desired instance.
Based on the URL path in the incoming request (e.g., /app1, /app2), it forwards the request to different target groups.
app1

![WhatsApp Image 2025-05-31 at 02 51 49_87abb820](https://github.com/user-attachments/assets/2156e644-2477-4262-8c07-bacc584c2ae5)


app2

![WhatsApp Image 2025-05-31 at 02 53 02_2595a180](https://github.com/user-attachments/assets/39aac217-7c69-470d-a1f8-e9f40a747fea)
