
# AWS-EC2-Instances
Module to create multiple instances with the same cofiguration

### Usage examples
```terraform
#Using var file
module "ec2" {
  source        = "../readme-ec2-instances"
  quantity      = var.quantity
  ami           = var.ami
  instance_type = var.instance_type
  key_name      = var.key_name
  subnet_id     = var.subnet_id
}

#Using values
module "ec2" {
  source        = "../readme-ec2-instances"
  quantity      = 6
  ami           = "ami-052efd3df9dad4825"
  instance_type = "t2.micro"
  key_name      = "key-ubuntu"
  subnet_id     = "subnet-08f1c81227a0e41f6"
}
```

## Examples
- [Basic](url)

## Requirements

|Name     |Version |
|---------|--------|
|terraform|>=0.13.0|

## Providers
No provider

## Inputs

|Name         |Description                    |Type         |Default|Required|
|-------------|-------------------------------|-------------|-------|--------|
|count        |number of instances to create  |`number`     |`null` |no      |
|ami          |Image of instance              |`string`     |`null` |yes     |
|instance_type|Type of instance               |`string`     |`null` |yes     |
|key_name     |Key-pair name                  |`string`     |`null` |yes     |
|subnet_id    |VPC subnet ID                  |`string`     |`null` |yes     |
|tags         |Tags for your resources        |`map(string)`|`null` |no      |