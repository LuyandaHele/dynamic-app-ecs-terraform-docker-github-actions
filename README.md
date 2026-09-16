This project demonstrates the architectural design , build and deployment of a automated CI/CD pipeline for a dynamic website application hosted on AWS using Github Actions, Terraform , Docker , Amazon ECR and Amazon ECS Fargate.
It builds upon  a highly available AWS infrastructure architecture with an automated deployment workflow that enables application changes to be built , containerized , stored and deployed to AWS through a repeatable CI/CD process.
The pipeline integrates Github Actions with AWS to automate infrastructure provisioning through Terraform , Docker image creation, Amazon ECR for image management and ECS for application deployments.

The project and solution built demonstrates practical DevOps and cloud engineering practices including Infrastructure as Code, containerization, continuous integration, continuous deployment , cloud automation and version-controlled application delivery.

Key Features : 

Automated CI/CD pipeline using Github Actions
Infrastructure provisioning using Terraform
Docker containerization of the web application
Amazon ECR for container image storage
Amazon ECS Fargate for container deployment
Ephemeral ECS self-hosted Github Actions runner
Automated ECS task definition revision creation
Automated ECS service deployment and restart
Multi-AZ AWS Infrastructure
Public and private subnet separation
Application Load Balancer for traffic distribution
NAT Gateways for outbound creativity 
Multi-AZ Amazon RDS architecture
Github-based source control and version management

CI/CD Pipeline
The pipeline automates the application deployment process from source code to a running ECS Service

Source Control --> Developers commit and push application and infrastructure changes to Github using Git.

Github Actions --> A Github Actions workflow is triggered to automate the deployment process.

AWS authentication --> Github Actions authenticates with AWS using configured AWS credentials allowing the workflow to interact with the required AWS Services.

Infrastructure Provisioning --> Terraform is used to provision and manage the required AWS infrastructure in a repeatable and version controlled mannner.

Self-Hosted Runner --> Self-hosted Github Actions runner is started to execute the required container build and deployment tasks.

Docker Build --> The application is packaged into a Docker container image , providing a consistent environment for running the application. 

Amazon ECR --> The Docker image is pushed to an Amazon Elastic Container Registry (ECR) repository where it can be securely stored and retrieved by ECS.

ECS Deployment --> A new ECS Task definition revision is created using the updated container image and the ECS Service is updated to deploy the new application verison.

Runner Cleanup --> After completing the required CI/CD tasks the temporary ECS self-hosted runner is stopped
