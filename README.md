# Packer - AMI
## Project Description
Build AMI using packer
## Requirement
1. Packer
2. AWS account 
## Project set up
1. Clone the project using https://github.com/ashoka-fall2020/webapp.git
2. Install packer in your system. For Mac you can use the command `brew install packer`
3. In the terminal go to the `ami` directory
4. Validate packer using `packer validate ami.json`
5. Build AMI using the command 
 ````
packer build \ 
    -var 'aws_access_key=REDACTED' \
    -var 'aws_secret_key=REDACTED' \
    -var 'aws_region=us-east-1' \
    -var 'subnet_id=REDACTED' \
    -var 'ami_users=REDACTED' \
    ami.json`
 ````
## Deploy
1. Go to your AWS console and launch an EC2 instance with the new AMI