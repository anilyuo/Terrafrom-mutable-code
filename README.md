Terrafrom-mutable-code
# Mutable Infrastructure with Terraform
This repository contains Terraform code to provision a complete infrastructure setup on AWS using AMI images. The infrastructure includes the following components:

Virtual Private Cloud (VPC)
Subnets (public and private)
Internet Gateway
NAT Gateway
Security Groups
Application Load Balancer (ALB)
Target Group
Auto Scaling Group

# Overview
The goal of this project is to showcase how to leverage AMI images to provision a mutable infrastructure setup. By using AMI images, you can easily deploy pre-configured instances with your desired software stack and configurations. This approach allows for faster and more consistent deployments, as well as the ability to quickly scale your infrastructure based on demand.
# Prerequisites
Before you can use this Terraform code, you'll need to have the following:

AWS account and credentials configured
Terraform installed on your local machine

# Usage

Clone this repository to your local machine.
Navigate to the project directory.
Initialize Terraform by running terraform init.
Review the variables.tf file and update any necessary variables (e.g., AWS region, instance type, AMI ID).
Create a plan for the infrastructure changes by running terraform plan.
If the plan looks correct, apply the changes by running terraform apply.

Terraform will provision the entire infrastructure based on the configurations defined in the code. This includes creating the VPC, subnets, security groups, load balancer, target group, and auto scaling group. The auto scaling group will launch instances based on the specified AMI image.
# AMI Images
In this project, we're using custom AMI images that have been pre-configured with the necessary software and configurations. These AMI images can be created manually or through automation tools like Packer.
By using pre-configured AMI images, we can ensure that all instances launched within the auto scaling group are consistent and meet our desired specifications. This approach simplifies the deployment process and reduces the risk of configuration drift.
# Cleanup
To remove the provisioned infrastructure, run terraform destroy. This will delete all the resources created by Terraform, including the VPC, subnets, security groups, load balancer, target group, and auto scaling group.
