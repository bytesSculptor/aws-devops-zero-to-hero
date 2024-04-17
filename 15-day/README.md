
# Day-15 | AWS ULTIMATE CICD PIPEPLINE | END TO END DEMO | AWS CODE PIPELINE 

## AWS CodeDeploy Setup


- Create a T2 micro [[Amazon Elastic Compute Cloud | EC2]] instance with a public IP and enable [[Secure Shell | SSH]].
- Use tags to identify and manage resources.
- Install the CodeDeploy agent on each EC2 instance.
- Follow AWS documentation to install Ruby, wget, and the CodeDeploy agent.
- Replace bucket name and region identifier in the install script with region-specific values.
- Grant permissions to the install script and run it to complete agent installation.



## Configuring EC2 Instance for CodeDeploy


- Create an IAM role for the [[Amazon Elastic Compute Cloud | EC2]] instance to allow communication with CodeDeploy.
- Configure the CodeDeploy application to use the EC2 instance as a deployment target.



## Setting Up a Deployment


- Create an abstract.yaml file and place it in the root of the [[GitHub]] repository.
- Authenticate with GitHub and provide the repository name and commit ID if using a GitHub repository.
- Place the app spec.yaml file at the root of the GitHub repository.
- Check the View events section if the deployment process fails to see if the file was fetched successfully.
- Convert the repository to a [[Visual Studio Code]] setup for easy editing using the . (dot) button on GitHub.
- Create a scripts folder and add stopcontainer.sh and startcontainer.sh files to control the Docker container.
- Add Docker pull and run commands to the startcontainer.sh file.



## Troubleshooting Deployment Issues


- Install Docker if the deployment fails due to the Docker command not being found.
- Use tags when pushing and pulling images to ensure the correct version of the image is deployed.



## Automating Deployment with CodePipeline


- Add a CodeDeploy stage to the CodePipeline to automate the deployment process.



## Resolving Port Conflict Issue


- Change the port binding in the startcontainer.sh script or forcefully delete the running container using Docker RM -f if the deployment fails due to a port conflict.
- Write a script to stop the running container using Docker PS, awk, and Docker RM -f.

