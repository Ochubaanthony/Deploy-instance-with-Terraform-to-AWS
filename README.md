# Deploy-instance-with-Terraform-to-AWS
Steps to deploy EC2 Instance with Terraform


HOW TO CREATE AWS INSTANCE

STEPS
GO TO AWS CONSOLE AND SEARCH FOR IAM 
Click create user
After create user click on the user and click credentials > 
Create access account 
Copy both access

Step 
Move to VSCODE
Create a folder Terraform
On the terminal
Type aws configure
Paster the both access key

Step
Create a file under the folder of Terraform
Main.tf

Paster this code below

provider "aws" {
    region = "us-east-1"
  
}

resource "aws_instance" "my_instance" {
    ami = "ami-0953476d60561c955"                         depending on the type of images you want this image is for Amazon
    instance_type = "t2.micro"
    tags = {
        "Name" = "MyEC2Instance"

    }

  
}


Step
Terraform fit
Terraform init
Terraform validate
Terraform plan
Terraform apply

Steps
Go to aws console to validate
Search for ec2 instance 


Step
If you want to terminal the instance you created
Go back to the vscode

Terraform destroy


