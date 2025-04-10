# Terraform Basics

## What is Terraform?
Terraform is an open-source Infrastructure as Code (IaC) tool created by HashiCorp.  
It allows you to define, provision, and manage infrastructure across multiple cloud providers using a declarative configuration language called HashiCorp Configuration Language (HCL).

---

## Terraform Core Concepts

> **Providers**:  
> Plugins that allow Terraform to interact with cloud providers (like AWS, Azure, GCP) or other APIs.

> **Resources**:  
> Components that Terraform manages, such as virtual machines, storage accounts, or networking services.

> **Variables**:  
> Allow you to make your Terraform code dynamic and reusable.

> **Outputs**:  
> Display information after your Terraform run, such as IP addresses or URLs.

> **State File**:  
> Terraform keeps track of the infrastructure it manages using a state file (`terraform.tfstate`).  
> This file maps your configuration to real-world resources.

> **Modules**:  
> Containers for multiple resources that are used together. Modules can be reused across projects.

> **Provisioners**:  
> Allow you to execute scripts or commands on a local or remote machine after a resource is created.

---

## Basic Terraform Workflow

1. **Write Configuration**:  
   Define infrastructure in `.tf` files using HCL.

2. **Initialize** (`terraform init`):  
   Initialize the working directory by downloading the necessary provider plugins.

3. **Validate** (`terraform validate`):  
   Check whether the configuration is valid.

4. **Plan** (`terraform plan`):  
   Preview the changes Terraform will make without applying them.

5. **Apply** (`terraform apply`):  
   Apply the changes to reach the desired infrastructure state.

6. **Destroy** (`terraform destroy`):  
   Remove all the infrastructure managed by Terraform.

---

## Common Terraform Commands

| Command              | Description                           |
|----------------------|---------------------------------------|
| `terraform init`     | Initialize the working directory.     |
| `terraform validate` | Validate the configuration.           |
| `terraform plan`     | Preview changes before applying.      |
| `terraform apply`    | Apply the changes.                    |
| `terraform destroy`  | Destroy all managed infrastructure.   |

---

## Terraform Best Practices

> **Use Remote Backend for State Files**:  
> Always store `terraform.tfstate` in a remote backend like S3 with DynamoDB locking to avoid losing important data.

> **Always Version Control**:  
> Save `.tf` files in a version control system like Git to track changes and collaborate easily.

> **Use Variables and Outputs Wisely**:  
> Keep your configurations modular, reusable, and easy to maintain.

> **Write Modular Code**:  
> Break down your Terraform code into modules to promote reusability and scalability.

> **Enable State Locking**:  
> Prevent concurrent operations on the same infrastructure by enabling state locking.

> **Keep Sensitive Data Secure**:  
> Never hardcode secrets or passwords. Use environment variables, Vault, or other secret management tools.

> **Format and Validate Code**:  
> Always run `terraform fmt` and `terraform validate` before pushing your code.

---

