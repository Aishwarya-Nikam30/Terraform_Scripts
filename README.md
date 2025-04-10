# Terraform Basics
## What is Terraform?
Terraform is an open-source Infrastructure as Code (IaC) tool created by HashiCorp.
It allows you to define, provision, and manage infrastructure across multiple cloud providers using a declarative configuration language called HashiCorp Configuration Language (HCL).

## Terraform Core Concepts
Providers:
Providers are plugins that allow Terraform to interact with cloud providers (like AWS, Azure, GCP) or other APIs.

Resources:
Resources are the components that Terraform manages, such as virtual machines, storage accounts, or networking services.

Variables:
Variables allow you to make your Terraform code dynamic and reusable.

Outputs:
Outputs are used to display information after your Terraform run, such as IP addresses or URLs.

State File:
Terraform keeps track of the infrastructure it manages using a state file (`terraform.tfstate`).
This file maps your configuration to the real-world resources.

Modules:
A module is a container for multiple resources that are used together. Modules can be reused across projects.

Provisioners:
Provisioners allow you to execute scripts or commands on a local or remote machine after a resource is created.

## Basic Terraform Workflow
1. Write Configuration:
Define infrastructure in `.tf` files using HCL.

2. Initialize (`terraform init`):
Initialize the working directory by downloading the necessary provider plugins.

3. Validate (`terraform validate`):
Check whether the configuration is valid.

4. Plan (`terraform plan`):
Preview the changes Terraform will make without applying them.

5. Apply (`terraform apply`):
Apply the changes to reach the desired infrastructure state.

6. Destroy (`terraform destroy`):
Remove all the infrastructure managed by Terraform.
