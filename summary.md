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


## 