# Terraform AWS Infrastructure


A hands-on Infrastructure as Code (IaC) project that provisions AWS infrastructure using Terraform.


This project demonstrates how Terraform can be used to create, configure, and manage AWS networking and compute resources in a repeatable and automated way.


---


## 📌 Project Overview


The project provisions a basic AWS environment consisting of:


- Amazon VPC
- Public Subnet
- Internet Gateway
- Public Route Table
- Route Table Association
- Security Group
- Amazon EC2 Instance
- Ubuntu AMI using Terraform Data Source


The infrastructure is completely defined as code using Terraform.


---


## 🏗️ Architecture


```text
                         AWS
                          |
                    +-----+------+
                    |    VPC     |
                    | 10.0.0.0/16|
                    +-----+------+
                          |
                    Public Subnet
                    10.0.1.0/24
                          |
                +---------+---------+
                |                   |
        Internet Gateway      Security Group
                |                   |
                +---------+---------+
                          |
                     EC2 Instance
                       t2.micro
                        Ubuntu

```

---
## 🛠️ Technologies Used

 
| Technology | Purpose |
|---|---|
| Terraform | Infrastructure as Code |
| AWS VPC | Network infrastructure |
| AWS EC2 | Compute / virtual server |
| AWS Subnet | Network segmentation |
| Internet Gateway | Internet connectivity |
| Route Table | Network traffic routing |
| Security Group | Instance-level firewall |
| Ubuntu | EC2 operating system |

---
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
```
---
### 📄 File Description

| File | Description |
|---|---|
| `main.tf` | Defines AWS infrastructure resources such as VPC, subnet, Internet Gateway, route table, security group, and EC2 |
| `provider.tf` | Configures the AWS provider and AWS region |
| `variables.tf` | Defines reusable Terraform variables |
| `terraform.tfvars.example` | Provides example values for Terraform variables |
| `.gitignore` | Prevents Terraform state and sensitive/local files from being committed |
| `.terraform.lock.hcl` | Locks Terraform provider versions |
| `README.md` | Contains project documentation |

---
## ⚙️ Prerequisites

Before running this project, make sure you have the following installed and configured:

- **Terraform**
- **AWS CLI**
- **Git**
- **An AWS account**
- **An AWS EC2 Key Pair**

---
### 🔑 Configure AWS Credentials

Configure your AWS credentials using the AWS CLI:

```bash
aws configure
```

You will be prompted for:

```text
AWS Access Key ID
AWS Secret Access Key
Default region name
Default output format
```

For this project, the AWS region is:

```text
ap-south-1
```

> ⚠️ Never commit AWS access keys, secret keys, or other credentials to GitHub.

---
## 🚀 Deployment

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/dhivmunz/terraform-aws-infrastructure.git
```

### 2️⃣ Navigate to the Project

```bash
cd terraform-aws-infrastructure
```

### 3️⃣ Configure Variables

Create your local `terraform.tfvars` file:

```bash
cp terraform.tfvars.example terraform.tfvars
```

### 4️⃣ Validate the Configuration

```bash
terraform validate
```

Expected result:

```text
Success! The configuration is valid.
```

---

### 5️⃣ Review the Execution Plan

```bash
terraform plan
```

Terraform displays the infrastructure changes before making any changes to AWS.

---

### 6️⃣ Create the Infrastructure

```bash
terraform apply
```

Terraform will show the execution plan and ask for confirmation.

Type:

```text
yes
```

to approve the deployment.

---
## 🔄 Terraform Workflow

```text
Terraform Configuration
          |
          ↓
   terraform init
          |
          ↓
 terraform validate
          |
          ↓
   terraform plan
          |
          ↓
  terraform apply
          |
          ↓
  AWS Infrastructure
```

## 🔍 Verification

After deployment, verify that the infrastructure matches the Terraform configuration:

```bash
terraform plan
```

If there are no configuration changes, Terraform displays:

```text
No changes. Your infrastructure matches the configuration.
```

You can also inspect the resources managed by Terraform:

```bash
terraform state list
```

---

## 🧠 Key Terraform Concepts Practiced

This project provided hands-on experience with:

- Infrastructure as Code (IaC)
- Terraform Providers
- Terraform Resources
- Terraform Data Sources
- Terraform Variables
- Terraform State
- Terraform Dependency Management
- Terraform Plan
- Terraform Apply
- In-place resource updates
- Resource replacement
- AWS VPC networking
- Public Subnets
- Internet Gateway
- Route Tables
- Security Groups
- EC2 Provisioning
- Git and GitHub workflow

---

## 🔐 Security Considerations

Sensitive and local Terraform files are excluded from version control.

The following files are **not committed to GitHub**:

```text
terraform.tfvars
terraform.tfstate
terraform.tfstate.backup
.terraform/
```

Never commit sensitive information such as:

- AWS Access Keys
- AWS Secret Keys
- Private SSH Keys
- Passwords
- API Tokens

The `.gitignore` file is used to prevent sensitive and local Terraform files from being tracked by Git.

---

## 📚 What I Learned

Through this project, I gained practical experience in:

- Designing basic AWS infrastructure using Terraform
- Creating AWS networking components using Infrastructure as Code
- Provisioning EC2 instances with Terraform
- Using Terraform variables and data sources
- Understanding Terraform state
- Reviewing infrastructure changes using `terraform plan`
- Managing infrastructure using `terraform apply`
- Understanding the difference between in-place updates and resource replacement
- Managing Terraform code using Git and GitHub
- Following safe practices for excluding sensitive files from version control

---

## 👩‍💻 Author

### Dhivya Munusamy

**Aspiring Cloud & DevOps Engineer**

**Skills:**  AWS • Terraform • Linux • Docker • Jenkins • CI/CD • Git • GitHub
