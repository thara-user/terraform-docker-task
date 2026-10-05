\# Task 3 - Infrastructure as Code (IaC) with Terraform



\## Objective



The objective of this task was to provision a local Docker container using Terraform.



\## Tools Used



\- Terraform

\- Docker

\- Docker Provider

\- Nginx

\- GitHub



\## Project Description



In this task, Terraform was used as an Infrastructure as Code (IaC) tool to provision and manage a local Docker container.



The Docker provider was configured in Terraform, and an Nginx Docker image and container were created.



\## Container Details



\- Container Name: terraform-nginx

\- Docker Image: nginx:latest

\- Container Port: 80

\- Host Port: 8085

\- Application URL: http://localhost:8085



\## Project Structure



terraform-docker-task/

│

├── main.tf

├── README.md

└── screenshots/

&#x20;   ├── terraform-init.png

&#x20;   ├── terraform-validate.png

&#x20;   ├── terraform-plan.png

&#x20;   ├── terraform-apply.png

&#x20;   ├── docker-container.png

&#x20;   ├── terraform-state.png

&#x20;   └── terraform-destroy.png



\## Steps Performed



\### Step 1 - Initialize Terraform



Command:



terraform init



Purpose:



Initializes the Terraform working directory and downloads the required Docker provider.



Provider used:



kreuzwerker/docker



\### Step 2 - Validate Terraform Configuration



Command:



terraform validate



Purpose:



Checks whether the Terraform configuration is correctly written and valid.



\### Step 3 - Create Terraform Plan



Command:



terraform plan



Purpose:



Shows the changes Terraform will make before creating the infrastructure.



\### Step 4 - Create Infrastructure



Command:



terraform apply



Purpose:



Applies the Terraform configuration and creates the Docker resources.



Resources created:



\- Nginx Docker image

\- Nginx Docker container



Container created:



terraform-nginx



\### Step 5 - Verify Docker Container



Command:



docker ps



Purpose:



Checks whether the Docker container is running.



The container was running with the following port mapping:



0.0.0.0:8085 -> 80/tcp



The Nginx application was tested in a browser using:



http://localhost:8085



The Nginx welcome page was successfully displayed.



\### Step 6 - Check Terraform State



Command:



terraform state list



Purpose:



Displays the resources currently managed by Terraform.



Resources shown:



docker\_container.nginx

docker\_image.nginx



\### Step 7 - Display Terraform Details



Command:



terraform show



Purpose:



Displays detailed information about the Terraform-managed infrastructure.



\### Step 8 - Destroy Infrastructure



Command:



terraform destroy



Purpose:



Destroys the infrastructure created by Terraform.



The destroy operation completed successfully.



Result:



Destroy complete! Resources: 2 destroyed.



After destruction, the Docker container was no longer running.



\## Verification



The project was verified using:



docker ps



and:



terraform state list



The Nginx application was also tested using:



http://localhost:8085



\## Result



The local Nginx Docker container was successfully:



1\. Provisioned using Terraform

2\. Verified using Docker

3\. Tested through a web browser

4\. Tracked using Terraform state

5\. Destroyed using Terraform



\## Terraform Workflow



The complete workflow used in this task was:



terraform init

&#x20;       ↓

terraform validate

&#x20;       ↓

terraform plan

&#x20;       ↓

terraform apply

&#x20;       ↓

docker ps

&#x20;       ↓

terraform state list

&#x20;       ↓

terraform show

&#x20;       ↓

terraform destroy



\## Conclusion



This task demonstrated the basic Infrastructure as Code workflow using Terraform and Docker.



Terraform was successfully used to provision, verify, manage, and destroy a local Nginx Docker container.



The task was completed successfully.

