# Summary of AWS Notes

## Introduction to AWS and Public Cloud

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