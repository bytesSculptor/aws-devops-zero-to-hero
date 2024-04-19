# Day-11 | IaC with AWS CFT | Tips and Tricks to Write CFT | CFT vs Terraform

## Introduction [(00:00:00)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=0s)

- Abhishek introduces the topic of AWS CloudFormation Templates (CFT) and Infrastructure as Code (IaC).
- CFT implements the principles of IaC, unlike AWS CLI.

## AWS CFT [(00:02:55)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=175s)

- CFT stands for CloudFormation Templates and helps in creating, managing, and updating cloud infrastructure on AWS.
- CFT implements the principle of IaC, which means writing code to create infrastructure instead of using tools like AWS CLI.
- IaC makes CFT a preferred choice over AWS CLI in many cases.

## Infrastructure as Code Principle [(00:05:37)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=337s)

- Infrastructure as Code (IaC) tools, such as AWS CloudFormation Template (CFT), act as intermediaries between users and cloud providers by converting declarative and versioned templates into API calls that the cloud provider understands.
- CFT supports only AWS and converts YAML or JSON templates into AWS API calls.
- IaC templates should be declarative, describing the desired state of the infrastructure, and versioned, allowing for tracking changes over time.
- CloudFormation templates are easy to read, understand, and write, making them suitable for code review and auditing.

## When to use CFT [(00:13:13)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=793s)

- Use CLI for quick actions or simple scripts.
- Use CFT to create actual resources or large tags.

## Features of CFT [(00:14:47)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=887s)

- Supports both JSON and YAML formats.
- YAML is more widely used in DevOps and has advantages over JSON:
- Supports commenting, making it easier to understand the code.
- More readable due to indentation-based structure.
- Less complex compared to JSON.
- Teams mostly use YAML for writing CloudFormation templates.
- JSON can also be used, but it has limitations:
- Does not support commenting, making it harder to understand the code.
- Less readable due to bracket-based structure.

## Drift Detection [(00:17:55)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1075s)

- CFT has a feature called drift detection.
- Drift detection helps identify unintended changes made to infrastructure created through CloudFormation templates.
- By periodically running drift detection, users can detect and fix differences between the desired and actual state of the infrastructure.
- To submit a YAML file to AWS CFT, users can use the AWS CLI or the UI.
- In the CFT service, users can create a stack and import the YAML file from their personal laptop.
- This process allows users to submit their CloudFormation templates to AWS for infrastructure creation and management.

## CFT Structure [(00:21:37)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1297s)

- CFT has a specific structure for writing templates in YAML or JSON.
- Basic components of a CFT template:
- Version: Standard and cannot be changed.
- Description: Describes the purpose of the CFT.
- Metadata: Optional information about the owner or additional details.
- Parameters: Variables that can be passed to the CFT during runtime.
- Rules: Validates the parameters submitted by the user.
- Mappings: Assigns parameters to variables.
- Conditions: Allows for conditional statements in the template.
- Resources: Mandatory section where you define the resources to be created (EC2 instances, S3 buckets, etc.).
- Outputs: Optional section to define outputs for the template.
- The documentation for CloudFormation templates provides clear guidance on the structure and components.
- [[Visual Studio Code]] will be used for writing the templates, along with helpful plugins.

## CFT Documentation [(00:26:05)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1565s)

- AWS CFT has extensive documentation with theory and examples.
- The documentation covers template formats, template anatomy, and sample templates.

## Sample Template [(00:27:20)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1640s)

- Sample template provided for creating an EC2 instance in the default VPC.
- Users can copy and modify the template to create their own EC2 instances.

## Template Version [(00:28:07)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1687s)

- AWS template format version has remained the same for the past 13 years.
- Users can keep the version as it is for any project in their DevOps team.

## Template Anatomy [(00:28:35)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1715s)

- Template anatomy explains the entire format of the template, whether it's JSON or YAML.
- It includes template format version, description, metadata, parameters, and resources.

## Parameter [(00:29:37)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1777s)

- The resources field in a CloudFormation template specifies the resources to be created.
- Each resource starts with a name, but the actual type is specified in the Type field.
- Parameters can be used to populate values at runtime, allowing the same template to be used for different scenarios.

## Rules [(00:32:50)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=1970s)

- Rules can be defined for parameters to restrict the values that can be used.
- This can be useful to control costs or ensure that resources meet specific requirements.

## Mappings [(00:34:04)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2044s)

- Mappings can be used to map variables to parameters.
- This makes it easier to read and understand the template.

## Conditions

- Conditions can be used to control when a template is executed.
- For example, a template could be restricted to only running in a specific environment.

## Conditions [(00:34:44)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2084s)

- You can use parameters to set conditions for executing the template.
- For example, you can specify that the template should only be executed for a production environment.

## Resources [(00:35:17)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2117s)

- Resources are the only mandatory field in a CloudFormation template.
- Resources are grouped together in the Resources section of the template.
- Each resource has a configuration that specifies its properties.

## Outputs [(00:36:28)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2188s)

- Outputs allow you to define what information you want to receive after the template is executed.
- For example, you can specify that you want the public IP address of a created EC2 instance.

## Documentation [(00:37:11)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2231s)

- The CloudFormation documentation provides detailed information about the template anatomy and troubleshooting.
- It is recommended to review the documentation after watching the video to gain a deeper understanding of CloudFormation templates.

## AWS Console [(00:37:34)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2254s)

- To execute a CloudFormation template, you can use the AWS Console.
- In the AWS Console, search for "CloudFormation" and select the "Create stack" option.
- You can either upload a ready template, use a sample template, or create a template in the designer.
- [[AWS CloudFormation]] provides sample templates, but the CloudFormation templates documentation offers more comprehensive examples for specific resources.

## Template References [(00:39:52)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2392s)

- AWS provides examples of resource properties for all its services in the template references section.
- For example, the syntax for creating an EC2 instance can be found in the Amazon EC2 section.
- Users can ignore unnecessary parameters and focus on the required ones.

## Template Parameters [(00:40:42)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2442s)

- The template parameters section lists all possible parameters for a resource.
- Users can ignore irrelevant parameters and only use the required ones.

## Create Template in Designer [(00:41:01)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2461s)

- The create template in designer feature is useful for beginners who are not familiar with writing YAML files.
- It provides a drag-and-drop interface to create CloudFormation templates.
- Users can select resources from a list and the corresponding YAML code is automatically generated.
- The generated code can be edited and customized as needed.

## AWS Documentation [(00:44:47)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2687s)

- Search for the service in the AWS CloudFormation documentation under the "Template reference" section.
- Find the resource you want to create (e.g., S3 bucket) and copy the required parameters and properties from the documentation.
- Paste the copied parameters into the CloudFormation template designer or use indentation for YAML templates.

## Upload CFT Template [(00:47:24)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2844s)

- Create a stack and upload the CloudFormation template from your local computer or an S3 bucket.
- Provide a name for the stack and specify any parameters required by the template.
- Click on "Submit" to initiate the resource creation process.
- CloudFormation will take a few minutes to create the resources defined in the template.

## S3 Bucket [(00:49:44)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=2984s)

- CloudFormation automatically creates an S3 bucket to store the CloudFormation templates.
- The bucket name is randomly generated by AWS.
- Users can delete the S3 bucket without deleting the CloudFormation template or stack.

## Drift [(00:52:01)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=3121s)

- CloudFormation can detect drift, which is when the actual state of resources differs from the desired state defined in the template.
- Drift detection can be used to identify manual changes made to resources outside of CloudFormation.
- The drift status can be viewed in the stack options.

## Enable Versioning [(00:53:59)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=3239s)

- To enable bucket versioning, users can copy and paste the example configuration from the AWS documentation into their YAML template.
- The example configuration includes the VersioningConfiguration property with the Status set to Enabled.

## Create Cloud Formation Template [(00:55:32)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=3332s)

- Updated the cloud formation template and saved it in the downloads folder.
- Created a new stack named "test S3 bucket drift detection" using the updated template.
- Specified the IAM role to be used for the stack.
- Initiated the stack creation process.
- S3 bucket was created successfully.
- Versioning was enabled in the S3 bucket as specified in the template.
- Manually changed the versioning status to "suspend" to demonstrate drift detection.

## Drift Detect [(00:57:29)](https://www.youtube.com/watch?v=ov4WmWgQgsA&t=3449s)

- Drift detection in AWS CloudFormation helps identify resource changes and ensures they align with the desired state, allowing DevOps engineers to quickly address manual changes or misconfigurations.
- To efficiently write CloudFormation templates, install the YAML and AWS Toolkit plugins in [[Visual Studio Code]] for YAML file correction and AWS interaction features.
- The AWS template format version, description, resource name, resource type, and resource properties can be found by searching for specific keywords in Visual Studio Code.
- The mandatory properties for an EC2 instance are the image ID, key value, and security group.
- Parameters and conditions can be used in CloudFormation templates, but it is not recommended for beginners.
- CloudFormation templates are used to create and manage AWS resources, while [[Terraform (software) | Terraform]] is better suited for hybrid or multi-cloud environments and Crossplane is a competitor in the sandbox project phase.
- Organizations dedicated to AWS can use CloudFormation templates, while those considering other clouds may prefer Terraform.
