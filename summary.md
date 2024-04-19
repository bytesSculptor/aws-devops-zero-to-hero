# Summary of AWS Notes

## 01 Introduction to AWS and Public Cloud

- **Cloud Computing**: Cloud computing means using internet-based services to access resources like servers and storage. It's more cost-effective and efficient than traditional methods.
- **Public Cloud vs. Private Cloud**: Public cloud is shared and managed by third-party providers like AWS, while private cloud is exclusive to one organization and managed by them.
- **Why Public Cloud**: Public cloud is popular because it saves organizations from managing their own data centers and offers easy access to resources.
- **Why AWS**: AWS is popular because it was one of the first cloud providers and has a wide range of services. Learning AWS can lead to job opportunities.
- **Creating an AWS Account**: To start using AWS, you need to create an account on their website. They offer a free tier for beginners to explore their services.

**Key Points**:
- Cloud computing allows easy access to resources over the internet.
- Public cloud is managed by third-party providers, while private cloud is managed by the organization itself.
- AWS is popular for its wide range of services and job opportunities.
- Creating an AWS account is the first step to learning and using AWS services.

## 02 AWS IAM deep dive

**AWS IAM (Identity and Access Management)**

- **IAM Overview**: IAM is a service by AWS for managing access to AWS resources. It helps control who can access resources and what actions they can perform.
- **IAM Components**:
  - *Users*: Represent individual entities that interact with AWS resources. Each user has unique security credentials for authentication.
  - *Groups*: Collections of users with similar access requirements. Permissions can be assigned to groups for easier management.
  - *Roles*: Used to grant temporary access to AWS resources. Typically used by applications or services.
  - *Policies*: Define permissions in JSON format. They specify actions allowed or denied on specific AWS resources.

**Key Features**:
- **Least Privilege**: Users and entities are given only the permissions required for their tasks, reducing security risks.
- **Multi-factor Authentication (MFA)**: Provides an extra layer of security by requiring users to provide two forms of authentication.
- **Audit Trail**: Tracks user activity and changes to permissions for accountability and compliance purposes.

**Benefits**:
- **Security**: IAM helps secure AWS resources by controlling access and enforcing security policies.
- **Ease of Management**: Groups and roles make it easier to manage permissions for users and entities.
- **Compliance**: IAM helps meet compliance requirements by providing detailed access controls and audit capabilities.

IAM is crucial for managing access to AWS resources securely and efficiently, ensuring that only authorized individuals and services have access.


## 03 EC2

**Introduction to EC2 (Elastic Compute Cloud)**

- **What is EC2**: Amazon EC2 is a service that lets you use virtual computers in the cloud.
- **Key Features**: It's reliable, scalable, and secure, with options to save money and improve performance.
- **Use Cases**: EC2 is used for various tasks like running websites, databases, or scientific simulations.

**EC2 Instance Types**

- **General Purpose**: Good for a wide range of tasks like web servers or testing environments.
- **Compute Optimized**: Best for tasks that need a lot of processing power, like gaming servers.
- **Memory Optimized**: Great for tasks that need a lot of memory, like big data analytics.
- **Storage Optimized**: Ideal for tasks that need fast access to large amounts of data, like data warehousing.

**Instance Families**

- These are groups of instances designed for specific purposes, like computing (C) or storage (D).
- Some instances have special capabilities, like support for specific processors or high-performance networking.

**EC2 Instance Basics**

- Virtual servers you can use in the cloud.
- Important parts include AMI (the software for your server), instance types (like the size of your server), and instance states (whether your server is running or stopped).

**Launching an EC2 Instance**

- Steps for setting up and launching a virtual server using the AWS Management Console.
- Configuring details like the type of server, network settings, and storage options.

**Managing EC2 Instances**

- Controlling your virtual servers by starting, stopping, and deleting them.
- Checking how well your servers are running and fixing any issues.
- Accessing your servers securely using SSH.

## 04 VPC

A VPC is like your own private, secure space in the cloud where you can run applications and store data. It's like having your own internet within the bigger internet. You can create subnetworks (subnets) within your VPC to organize your resources. You can control who can access your resources and how they can communicate by setting up rules and security measures. You can connect your VPC to the internet or other networks using gateways. Overall, a VPC gives you control over your network environment in the cloud.

Key Components of a VPC:

1. **VPC**: Your virtual network in the cloud.
2. **Subnets**: Ranges of IP addresses within your VPC.
3. **IP Addressing**: Assigning IP addresses to your VPC and subnets.
4. **Network Access Control List (NACL)**: A firewall for controlling traffic at the subnet level.
5. **Security Group**: A firewall for controlling traffic at the instance level.
6. **Routing**: Determining where network traffic is directed.
7. **Gateways and Endpoints**: Connecting your VPC to other networks or AWS services.
8. **Peering Connections**: Routing traffic between two VPCs.
9. **Traffic Mirroring**: Copying network traffic for monitoring.
10. **Transit Gateways**: Routing traffic between VPCs, VPNs, and AWS Direct Connect.
11. **VPC Flow Logs**: Capturing information about IP traffic in your VPC.
12. **VPN Connections**: Connecting your VPC to on-premises networks.

When you create an AWS account, AWS provides a default VPC, but you should create VPCs for specific applications or projects.

## 05 AWS Security using Security Groups and NACL
Security Groups and Network Access Control Lists (NACLs) are like virtual barriers that protect your AWS resources from unauthorized access. 

- **Security Groups** work at the level of individual servers (EC2 instances). They decide what traffic is allowed to go in and out of each server based on rules you set. For example, you can allow traffic only on specific ports or from certain IP addresses. Security Groups are smart; if you allow traffic in, it automatically allows the corresponding outbound traffic out. Changes you make to Security Groups take effect right away.

- **NACLs**, on the other hand, work at the level of groups of servers (subnets). They are like gatekeepers that decide which traffic is allowed to enter or leave a group of servers. Unlike Security Groups, NACLs are not as smart; if you allow traffic in, you have to separately allow the corresponding outbound traffic out. Changes to NACLs might take a bit of time to apply everywhere.

Both Security Groups and NACLs are important for keeping your AWS resources safe by controlling the traffic that can access them.

## 06 Route 53

**Route 53** is a service by AWS that helps map domain names to IP addresses, making it easier to access applications. It simplifies DNS management for AWS-hosted applications. Route 53 intercepts user requests and translates domain names to IP addresses of load balancers.

DNS is important because it allows users to access applications using easy-to-remember domain names instead of complex IP addresses. Route 53 provides DNS as a service for AWS services like EC2 or EKS.

**Domain registration** can be done through AWS or externally. Hosted zones are used to create DNS records, regardless of where the domain is purchased.

Route 53 can perform health checks to monitor the health of web applications or servers.

For further learning, AWS provides detailed documentation with practical examples about Route 53.


## 07 AWS Project Used In Production
- VPC demo project - [Youtube Tutorial Video](https://youtu.be/FZPTL_kNvXc)
- Detailed Steps: [Day-7 Readme](https://github.com/bytesSculptor/aws-devops-zero-to-hero/blob/main/07-day/README.md)

## 08 AWS Scenario Based Interview Question

- Ques + Answers: [Day-8 Interview q&a](https://github.com/bytesSculptor/aws-devops-zero-to-hero/blob/main/08-day/Interview_q&a.md)

## 09 AWS S3 Buckets
Amazon S3 (Simple Storage Service) is a cloud storage service by AWS (Amazon Web Services) that lets you store and retrieve data from anywhere on the web. It uses containers called "buckets" to organize your data. S3 offers high durability, scalability, security, and cost-effectiveness for storing various types of data.

**Key Features of S3:**

- **Durability and Availability**: S3 ensures high durability and availability for your data.
- **Scalability**: You can store and retrieve any amount of data without capacity constraints.
- **Security**: S3 provides encryption, access control, and audit logging for secure storage.
- **Performance**: S3 delivers high performance for data retrieval and storage operations.
- **Cost-effective**: S3 offers cost-effective storage options and pricing models.

**Creating and Configuring S3 Buckets:**

- **Creating a Bucket**: You can create an S3 bucket using the AWS Management Console, CLI, or SDKs. The bucket name must be unique globally.
- **Bucket Properties**: You can configure properties like versioning for keeping multiple versions of an object, and bucket-level permissions using IAM policies.

**Uploading and Managing Objects:**

- **Uploading Objects**: You can upload objects to S3 using various methods. Each object is assigned a unique key (name) within the bucket.
- **Object Metadata**: Object metadata contains additional information about each object, such as content type and encryption settings.
- **Lifecycle Management**: Define rules for transitioning objects between different storage classes or deleting them automatically based on criteria.

**Advanced Features:**

- **Storage Classes**: S3 offers different storage classes for different use cases and performance requirements.
- **Replication**: S3 replication enables automatic and asynchronous replication of objects between buckets in different regions.
- **Event Notifications and Triggers**: Configure actions when specific events occur in an S3 bucket, such as triggering AWS Lambda functions.

**Security and Compliance:**

- Ensure bucket policies, access control, and encryption settings are configured correctly.
- Encrypt data at rest using server-side encryption and enable encryption in transit using SSL/TLS.

**Management and Administration:**

- Use IAM roles and policies to manage access to S3 buckets.
- Interact with S3 programmatically using AWS SDKs or APIs.

**Troubleshooting and Error Handling:**

- Understand common S3 error messages and their resolutions.
- Use tools like AWS CloudTrail and S3 access logs to identify and troubleshoot access problems.

Amazon S3 provides a reliable, secure, and scalable storage solution for a wide range of use cases, making it a popular choice for storing and managing data in the cloud.



## 10 AWS CLI Deep Dive

### AWS CLI (Command Line Interface)
- AWS CLI is a Python utility that allows users to automate AWS resource creation, management, and deletion through a command-line interface.
- AWS CLI simplifies the use of APIs by providing an abstraction layer that eliminates the need for complex code.
- AWS CLI acts as an intermediary between the user and AWS APIs, simplifying resource management.
- To install AWS CLI, follow the official AWS documentation and select the appropriate method based on your operating system.
- For Windows users, install Oracle VirtualBox and create a Linux virtual machine or install Git Bash for basic Linux commands and AWS CLI demonstrations.
- To authenticate AWS CLI, log in to your AWS account using the root user or IAM user.
- To verify installation, run `aws --version` in the terminal; a successful installation will display the version number.
- To configure AWS CLI, run AWS configure and provide the access key ID, secret access key, default region, and default output format.
- AWS CLI translates CLI commands into API calls that AWS understands.

### Using AWS CLI
- To list S3 buckets, run `AWS S3 ls`.
- To create an EC2 instance, use a command like `AWS ec2 run-instances --image-id ami-id --instance-type t2.micro --key-name key-name --security-group-ids sg-id`.
- To learn AWS CLI commands, refer to the AWS CLI Command Reference documentation.

### AWS CLI vs. Other Tools

- AWS CLI is useful for quick references and simple tasks like listing S3 buckets or creating EC2 instances.
- For more complex tasks, AWS CloudFormation templates or Terraform are better suited.

