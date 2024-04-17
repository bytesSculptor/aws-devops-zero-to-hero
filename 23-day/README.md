
# Day-23 | Secret Management on AWS | Most asked Interview question | #aws #abhishekveeramalla


## Chapter 1 [(00:00:00)](https://www.youtube.com/watch?v=FllcHYsBm78&t=0s)


- Abhishek introduces the topic of Secrets Management and its importance in [[DevOps]].



## Chapter 2 [(00:00:21)](https://www.youtube.com/watch?v=FllcHYsBm78&t=21s)


- Secrets Management is crucial in interviews, with 90% chance of being asked.
- Different services and tools are available for Secrets Management on [[Amazon Web Services | AWS]].



## Chapter 3 [(00:01:23)](https://www.youtube.com/watch?v=FllcHYsBm78&t=83s)


- As a DevOps engineer, handling sensitive information is crucial, such as [[Docker (software) | Docker]] credentials, database credentials, and AWS account access.
- Compromised secrets can lead to severe consequences for the organization.
- Secrets Management is a key responsibility of [[DevOps]] engineers.



## Chapter 4 [(00:02:56)](https://www.youtube.com/watch?v=FllcHYsBm78&t=176s)


- Three main options for Secrets Management on [[Amazon Web Services | AWS]]:
- Systems Manager Parameter Store
- Secrets Manager
- [[HashiCorp | HashiCorp Vault]] (not an AWS offering but widely used)
- Understanding when to use each option is important for interviews.



## Chapter 5 [(00:04:29)](https://www.youtube.com/watch?v=FllcHYsBm78&t=269s)


- Systems Manager (Parameter Store) is used to store sensitive information such as [[Docker (software) | Docker]] username, password, and registry URL.
- Information stored in Systems Manager can be easily retrieved by granting the [[Amazon Web Services | AWS]] service an [[Identity management | IAM]] role.



## Chapter 6 [(00:06:15)](https://www.youtube.com/watch?v=FllcHYsBm78&t=375s)


- Secrets Manager was introduced to automatically rotate sensitive information, reducing the risk of exposure or compromise.
- Secrets Manager can rotate certificates, passwords, and other sensitive information on a specified schedule.
- Systems Manager cannot automatically rotate sensitive information.



## Chapter 7 [(00:08:36)](https://www.youtube.com/watch?v=FllcHYsBm78&t=516s)


- Use Systems Manager for sensitive but not highly sensitive information such as [[Docker (software) | Docker]] username and registry URL.
- Use Secrets Manager for highly sensitive information such as Docker password and database passwords.
- Secrets Manager offers additional security configurations and password rotation policies but is slightly more expensive than Systems Manager.



## Chapter 8 [(00:09:57)](https://www.youtube.com/watch?v=FllcHYsBm78&t=597s)


- Systems Manager and Secrets Manager can be used together to optimize cost and security.
- Systems Manager is used for storing less sensitive information like usernames and registry URLs.
- Secrets Manager is used for storing highly sensitive information like passwords.
- Systems Manager offers various services like rotation and integration with Lambda functions for custom Secrets rotation policies.
- Using a combination of both Systems Manager and Secrets Manager allows for effective security measures while keeping cost optimization in mind.



## Chapter 9 [(00:14:14)](https://www.youtube.com/watch?v=FllcHYsBm78&t=854s)


- [[Amazon Web Services | AWS]] managed offerings tie users to the AWS platform, which can be a bottleneck for organizations using hybrid or multi-cloud environments or planning to migrate from AWS to another cloud provider.
- [[HashiCorp | HashiCorp Vault]] is a centralized Secrets management solution that can be used with AWS, [[Microsoft Azure | Azure]], or any other cloud platform.
- HashiCorp Vault is an open-source platform with a large community backup, providing many additional features and encryption strategies over AWS managed offerings.
- HashiCorp Vault is a good choice for organizations using multi-cloud environments or planning to migrate from AWS.

