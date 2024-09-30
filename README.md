# AWS Infrastructure Terraform Documentation

This repository contains Terraform scripts to create and manage AWS infrastructure.

## Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
  - [How to Apply Terraform](#how-to-apply-terraform)
  - [How to Destroy Infrastructure](#how-to-destroy-infrastructure)
- [Configuration](#configuration)
- [AWS Resources Created](#aws-resources-created)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The **AWS Infrastructure Terraform** project provides a set of Terraform modules to provision and manage a highly available, secure, and scalable AWS infrastructure.

The resources created may include:

- Virtual Private Cloud (VPC)
- Subnets
- Internet Gateway
- EC2 instances
- Security Groups

The project follows best practices for AWS infrastructure setup.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Terraform version `>= 1.x`
- AWS CLI configured with necessary access permissions
- An AWS account

## Getting Started

To set up this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/omar1593321/AWS_Infra_TerraForm.git
   cd AWS_Infra_TerraForm
   ```

2. Initialize the Terraform working directory:
   ```
   terraform init
   ```
   Define your AWS region and credentials in a .tfvars file (optional) or export them as environment variables.
## Usage
How to Apply Terraform
To create the infrastructure, use the following command:
```
terraform apply

```
This will provision all the resources specified in the Terraform files.

How to Destroy Infrastructure
If you need to destroy all resources created by Terraform, run:
## Configuration
Terraform Variables
The following are the variables you can configure in the project:

aws_region: Specify the AWS region where the infrastructure will be deployed.
instance_type: The type of EC2 instance to deploy.
vpc_cidr: The CIDR block for the VPC.
Other variables related to subnet CIDRs, key pairs, security groups, etc.

## AWS Credentials
Ensure that your AWS credentials are properly set up. You can do this using environment variables or by setting up the ~/.aws/credentials file:
```
export AWS_ACCESS_KEY_ID=your_access_key
export AWS_SECRET_ACCESS_KEY=your_secret_key
```
## AWS Resources Created
The following resources are created by this Terraform module:

VPC: A Virtual Private Cloud with the specified CIDR block.
Subnets: Public and private subnets distributed across availability zones.
EC2 Instances: Virtual machines in the public and private subnets.
Security Groups: To control inbound and outbound traffic for the instances.
You can modify the configuration to adjust the number of instances, instance types, and additional resources as needed.