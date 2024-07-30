
**Project Title**:  Resilient and Scalable Web Application Deployment on AWS </u>

**Project Description**

This project aims to design and implement a highly available and scalable infrastructure for a web application on AWS. The architecture will leverage AWS services to ensure the web application can eﬃciently handle varying loads and maintain high availability across multiple Availability Zones.


**Objectives**

High Availability: Achieve minimal downtime by utilising multiple Availability Zones.
Scalability: Use AWS Auto Scaling to adjust resources automatically in response to traﬃc changes.
Security: Implement security measures focusing on security groups and secure communication.
Resilience: Develop an application setup that can withstand failures and traﬃc spikes without manual intervention.


**Core AWS Services Utilisation**


-Virtual Private Cloud (VPC): Provides an isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you deﬁne.
Elastic File System (EFS): Offers a simple, scalable, elastic ﬁle storage for use with AWS Cloud services and on-premises resources.
Elastic Compute Cloud (EC2): Provides scalable computing capacity in the AWS cloud. It allows developers to scale up or down based on demand.
AWS Auto Scaling: Monitors applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.
Application Load Balancer (ALB): Automatically distributes incoming application traﬃc across multiple targets, such as EC2 instances, containers, and IP addresses.
 
**Architecture Overview**

VPC Setup
![VPC Design](https://github.com/user-attachments/assets/04d09613-d2cc-4200-a30e-0dec7eb9a2a2)



●	Diagram: Include a cloud architecture diagram showing the relationship between VPC, EFS, EC2 instances, Auto Scaling, ALB, and Route 53.



# Network Architecture Diagram: Ap-South-1  

This document provides an overview of the network architecture for the Ap-South-1 region, detailing the components and their relationships.  

## Diagram Overview   

### Components  

- **Virtual Private Cloud (VPC)**:   
  - CIDR Block: `192.168.0.0/24`  
  - The VPC serves as the isolated network environment.  

- **Internet Gateway**:   
  - Facilitates communication between the VPC and the internet.  

- **Route Table (RT)**:   
  - Manages the routing of traffic within the VPC.  

### Subnets  

1. **Public Subnets**:  
   - **Public_Subnet_1A**:   
     - CIDR Block: `192.168.0.0/26`  
     - Contains resources that need direct access to the internet.  
   - **Public_Subnet_2B**:   
     - CIDR Block: `192.168.0.64/26`  
     - Similar to Public_Subnet_1A, it hosts public-facing resources.
    - **RT_For_Public**:   
     - Manages routing for the public subnet.  

2. **Private Subnet**:  
   - **Private_Subnet_1A**:   
     - CIDR Block: `192.168.0.128/26`  
     - Hosts resources that do not require direct internet access.
    - **Private_Subnet_2B**:   
     - CIDR Block: `192.168.0.192/26`  
     - Hosts resources that do not require direct internet access.   
   - **Main Route Table (Main RT)**:   
     - Manages routing for the private subnet.  

### NAT Gateway  

- **NAT Gateway**:   
  - Allows instances in the private subnet to initiate outbound traffic to the internet while preventing inbound traffic from the internet.
### Note

   After the creation of the complete VPC architecture. Go to VPC - Action - Edit VPC Setting - Enable DNS Hostname

## Summary  

This architecture ensures a secure and efficient network setup, allowing for both public and private resources while maintaining control over internet access.


**●	Security Groups**

   •	Web-SG – To access Webserver  - (Allow all traffic from Anywhere) 
   
   •	ALB-SG – To access Load Balancer   - (Allow all traffic from Anywhere) -  
   
   •	EFS-SG – To access EFS   -  - (Allow all traffic from Anywhere) 
   
### Note


We allow All traffic from Anywhere to all Security Groups for temporary testing, they all will be edited with by following the best practices to enhance our security at last phase of our project completion.

 
### Elastic Compute Cloud (EC2)

Follow Implementation file

### Elastic File System (EFS)
Follow Implementation file

### Application Load Balancer (ALB)
Follow Implementation file

### 	Route 53
Follow Implementation file

### Application Deployment
Follow Implementation file

### Backup and Disaster Recovery
Follow Implementation file

### Troubleshooting
●	Common Issues: List common issues and their solutions.
●	Support: Information on how to get help or support.


Conclusion
This document outlines the initial design for deploying a resilient and scalable web application on AWS. It emphasizes high availability, scalability, security, and
resilience, leveraging AWS services to achieve these objectives. The next steps include detailed planning, implementation, testing, and deployment phases, ensuring the web application meets the outlined objectives.
