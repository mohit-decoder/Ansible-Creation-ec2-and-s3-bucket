Here's a complete README.md file that includes instructions for installing Ansible, creating an EC2 instance and an S3 bucket, as well as deleting them:
# Ansible EC2 Instance and S3 Bucket Configuration

This repository contains an Ansible playbook for creating an EC2 instance and an S3 bucket in AWS. Additionally, it includes instructions for deleting the EC2 instance and S3 bucket.

## Prerequisites

Before running the playbook, ensure that the following prerequisites are met:

- Ansible is installed on the system where you plan to run the playbook.
- AWS CLI is installed and configured with the appropriate credentials on the system.
- You have the necessary permissions in AWS to create and delete EC2 instances and S3 buckets.

## Installation

1. Install Ansible on your system:
       sudo apt update
       sudo apt install ansible
2. Install required Python libraries:
       sudo apt install python3-pip
       pip3 install boto boto3 botocore
3. Install the AWS CLI:
       sudo apt install awscli
4. Configure AWS credentials by running:
       aws configure

## Usage
Create EC2 instance and S3 bucket
1. Run the playbook to create the EC2 instance and S3 bucket:
    ansible-playbook create_ec2_s3.yml
2. The playbook will provision an EC2 instance and create an S3 bucket in the specified AWS region.

After the playbook execution, the EC2 instance's public IP will be displayed.

Delete EC2 instance and S3 bucket
1. Create Delete_ec2_s3.yml
2. after making changes in instance id and selecting the name of the bucket
3. run the command : ansible-playbook Delete_ec2_s3.yml

Notes:
Exercise caution when creating or deleting resources. Ensure that you have the necessary permissions and that you understand the implications of these actions.
Make sure to configure your AWS credentials properly, either by setting environment variables or using AWS CLI configuration.
Review and update the playbook variables as per your specific requirements before running the playbook.





