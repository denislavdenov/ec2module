# Module that creates EC2 instance and assigning random name using random name module

## V 0.0.1
**Module in module terraform code**

## V 0.0.2
**Adds travis kitchen-terraform test to previous code**

## V 0.0.3
**Updated terraform code so the EC2 has provisioning which removes the SSH timeout on the kitchen verify step**


# How to use:
1. You need to have your private key in the terraform code location
2. You need to set these variables:

```variable "aws_access_key" {
  type    = "string"
  default = ""
}

variable "aws_secret_key" {
  type    = "string"
  default = ""
}

variable "ami" {
  type    = "string"
  default = ""
}

variable "instance_type" {
  type    = "string"
  default = "t1.micro"
}

variable "public_key" {
  type    = "string"
  default = ""
}

variable "identity" {
  type    = "string"
  default = ""
}

variable "security_group_id" {
  type        = "string"
  description = "The AWS security group with ingress and egress rules for this instance."
  default     = ""
}
```
3. You need to have terraform installed
`terraform init`
`terraform apply`
4. You need kitchen installed for testing
`kitchen converge`
`kitchen verify`
`kitchen destroy`
