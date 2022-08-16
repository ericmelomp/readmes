# How to? - Terraform Module


This project consists of a module with the structure for creating an AWS Resource along with the resources needed to execute it. It also allows the configuration of each of these resources to be better inserted in your environment in a quickly and simply way, with Terraform. We are based on AWS Console and the official documentation https://registry.terraform.io/ for the creation of this module.

## Requirements

 - Install Terraform
 - Install Visual Studio Code
 - Install AWS CLI

## Download Links

- Terraform - https://www.terraform.io/downloads
- Visual Studio Code - https://code.visualstudio.com/?wt.mc_id=vscom_downloads
- AWS CLI - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

## Deploy

To deploy this project you have to clone the repository to your machine. In your command prompt, run:

```bash
  LINK
```
Open this repository with Visual Studio Code and look for `tfvars` file.

In `tfvars` insert the empty values that better correspond to your environment.

When everything is set, run:
- (You must be in the same diretory as all the files)

```bash
  terraform init
```

To initialize the backend

```bash
  terraform plan 
```

To create an `terraform.tfstate` and build a state to your resources. You'll be able to see all the resources and configurations that will be created, as well.

```bash
  terraform apply
```
To apply your resources in AWS. insert `yes` if you really want to apply them.

## Final Result

You can check if your resources were created as you wanted in the aws console. Go to https://aws.amazon.com/pt/console/ and see the created resources and configs.

![Logo](https://fcortes.com.br/static/1fa99d7351e4f4c5b4313e933de57031/d9199/terraform_logo.png)
### Extra commands

Here you'll see some commands the might help you:

```bash
    terraform destroy
```

Destroy all the resources created before.

```bash
    terraform validate
```

Check if you have something wrong with your code. (It doesn't avoid you for having trouble with the values of your configuration)

```bash
    terraform plan -out (file name)
```

Creates an specific file to your plan.
## Authors

- [TrendSolutions - Soluções Inteligentes](https://tsit.com.br/)