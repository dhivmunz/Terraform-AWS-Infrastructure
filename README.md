# Terraform AWS Infrastructure

## 📌 Project Overview

This project demonstrates how to provision AWS infrastructure using Terraform.

The infrastructure is created using Infrastructure as Code (IaC), allowing AWS resources to be defined, deployed, and managed through Terraform configuration files.

## 🏗️ Architecture

Terraform provisions the following AWS resources:

- VPC
- Public Subnet
- Internet Gateway
- Public Route Table
- Route Table Association
- Security Group
- EC2 Instance
- Ubuntu AMI using Terraform Data Source

## 📂 Project Structure

```text
terraform-aws-infrastructure/
│
├── main.tf
├── provider.tf
├── variables.tf
├── terraform.tfvars.example
├── .gitignore
├── .terraform.lock.hcl
└── README.md

⚙️ Technologies Used
Terraform
AWS
Amazon EC2
Amazon VPC
Ubuntu
Linux
Git
GitHub

🚀 Terraform Workflow
1. Initialize Terraform
	terraform init

2. Validate configuration
	terraform validate

3. Review execution plan
	terraform plan

4. Create infrastructure
	terraform apply

5. Check infrastructure changes
	terraform plan

Terraform should display:

No changes. Your infrastructure matches the configuration.


🔧 Variables

The project uses Terraform variables for configuration.

Example:

key_name = "your-ec2-key-pair-name"

Create your own terraform.tfvars file using terraform.tfvars.example.

The actual terraform.tfvars file is excluded from Git using .gitignore.

🧠 Key Terraform Concepts Practiced
Infrastructure as Code
Terraform Providers
Resources
Data Sources
Variables
Terraform State
Terraform Plan
Terraform Apply
In-place resource updates
Resource replacement
AWS networking
EC2 provisioning
Terraform dependency management

🔐 Security

Sensitive Terraform files and state files are excluded from version control.

The following files are intentionally not committed:

terraform.tfvars
terraform.tfstate
terraform.tfstate.backup
.terraform/
📚 Learning Outcome

This project provided hands-on experience with provisioning and managing AWS infrastructure using Terraform and understanding the Terraform workflow from configuration to deployment.

👩‍💻 Author

Dhivya Munusamy
