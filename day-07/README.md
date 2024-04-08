
# Day-7 | AWS Project Used In Production | Complete Implementation

## Chapter 1 [(00:00:00)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=0s)

- The project demonstrates how to create a secure VPC for production environments.
- The VPC **architecture** includes public and private subnets in two availability zones for redundancy.
- A NAT Gateway in the public subnet masks the IP addresses of applications when accessing the internet.
- An Auto Scaling Group launches applications in the private subnet, scaling up or down based on traffic load.
- A Load Balancer distributes traffic to applications in the private subnet, ensuring optimal resource utilization and high availability.
- Bastion (Jump Server) provides secure access to private subnet EC2 instances through the public subnet, facilitating logging, auditing, and traffic control for enhanced security.


## Chapter 2 [(00:08:02)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=482s)

- To create a VPC, go to the AWS console, search for VPC, and click on "Create VPC."
- Choose "VPC and more" to automatically create public and private subnets in multiple Availability Zones, along with route tables and other necessary configurations.
- Specify the project name, subnet configuration, IPv4 configuration, number of Availability Zones, number of public and private subnets, and NAT gateways.
- Deselect the VPC endpoint for the S3 bucket as it is not required for this project.
- Review the resources that will be created and click on "Create VPC."
- If the maximum number of elastic IP addresses is reached, release some elastic IP addresses from the EC2 console.
- Elastic IP addresses in AWS are static IP addresses that remain the same even if the instance is deleted.
- The VPC architecture created so far includes public subnets attached to a route table and internet gateway, and private subnets attached to different route tables.
- The next steps are to deploy EC2 instances with an auto-scaling group and add a load balancer.



## Chapter 3 [(00:16:05)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=965s)


- Auto scaling group cannot be created directly in AWS, a launch template is required.
- Launch template acts as a reference for understanding auto scaling group behavior.



## Chapter 4 [(00:16:45)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1005s)


- Create a launch template with the following configurations:
- Name: AWS broad example
- Operating System/AMI: Ubuntu
- Instance Type: Free tier
- Key Value Pair: Pick the desired key value pair
- Subnet Configuration: Create a new subnet
- Security Group: Create a new security group named AWS broad example
- VPC: Select the VPC created earlier
- Inbound Security Group Rules:
- SSH: Port 22, Source: Anywhere
- Application Port: Port 8000 (or as per application requirement), Source: Anywhere



## Chapter 5 [(00:20:05)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1205s)


- Configuring Auto Scaling Group:
- Similar to EC2 instance configuration.
- Auto Scaling Group scales EC2 instances.
- Refreshed the page to find the launch template.
- Selected VPC, availability zones, and subnets in the private subnet.
- Chose not to attach a load balancer.
- Specified desired capacity as 2 EC2 instances.
- Configured scaling options for automatic scaling up to 3 or 4 instances based on CPU monitoring.
- Notifications through SNS topics can be added for EC2 instance addition or termination.



## Chapter 6 [(00:23:05)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1385s)


- After a minute, the desired capacity and instances both became 2.



## Chapter 7 [(00:23:35)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1415s)


- Verified that the Auto Scaling Group created two instances, one in Us East 1A and the other in Us East 1B.
- Before creating the application load balancer, the application needs to be installed inside the servers.
- Bastion host is required to access the private subnet since the instances don't have public IP addresses.



## Chapter 8 [(00:25:35)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1535s)


- Created a Bastion host named "Bastion host" with Ubuntu image, T2 micro instance type, and AWS login key pair.
- Added a Security Group with SSH access to the Bastion host.
- Modified the network settings to ensure the Bastion host is created in the same VPC.
- Enabled auto-assign public IP address for the Bastion host.
- Launched the Bastion host instance.
- Plan to SSH to the Bastion host from a personal laptop and then SSH to the private subnet from the Bastion host.



## Chapter 9 [(00:27:20)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=1640s)


- To access private subnet instances, the Bastion host requires the SSH key value pair from the user's laptop.
- The SCP command securely copies the SSH key (AWS.pem) from the user's laptop to the Bastion host.
- After copying the SSH key, the user can log into private subnet instances using the private IP address and the SSH key.
- A Python application and an HTML page (index.html) are created and hosted on a private subnet instance.
- The Python server runs on port 8000 using the command "python3 -m *http.server* on port 8000".
- The demonstration aims to show that when using a load balancer, traffic will reach a specific instance and provide a response, while traffic directed to another application in a different subnet will receive an error indicating unavailability.
- The speaker will demonstrate load balancing using a Python application running on one EC2 instance.
- The goal is to distribute traffic evenly between two EC2 instances, with 50% of the traffic going to each instance.



## Chapter 10 [(00:33:50)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=2030s)


- Created an Application Load Balancer named "AWS prod example" in both public subnets.
- Configured the security group to allow SSH, port 8000, and port 80 traffic.
- Created a Target Group named "AWS prod example" with HTTP protocol and port 8000 and added the two EC2 instances to it.
- Added the target group to the load balancer by selecting the VPC, both subnets using the public option, and the security group that exposes Port 80 or Port 8000.
- Added load balancer tags and the target group to the Add-on Services.



## Chapter 11 [(00:41:50)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=2510s)


- The load balancer is not accessible because the subnet attached to it does not expose Port 80.
- To resolve the issue, allow HTTP traffic on the security group associated with the load balancer by adding a new inbound rule for port 80.
- After the configuration is reflected, the error should disappear, and the load balancer should be accessible from the internet.
- The target group actively monitors the healthy instances and forwards traffic only to the healthiest EC2 instance.
- To demonstrate load balancing, deploy the application on the second EC2 instance and observe that the load balancer alternates between displaying "This is my first AWS project" and "This is my second AWS project" when accessed.



## Assignment [(00:41:50)](https://www.youtube.com/watch?v=FZPTL_kNvXc&t=2510s)


- Deploy the application on the second EC2 instance with the message "This is my second AWS project".
- Verify that the load balancer alternates between displaying "This is my first AWS project" and "This is my second AWS project" when accessed.

