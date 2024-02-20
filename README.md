# hw4terra-aws
This terraform file allows a user to create a ec2 instance using the latest debian ami. It creates a security group allowing only ssh from a specified user cidr input. It allows a user to input a KMS key pair and outputs the public hostname.

USAGE:
clone files to a directory on your computer (git clone https://github.com/manuellalonzo/hw4terra-aws ). cd to the cloned directory
run from command line:

terraform init

terraform apply

then provide 3 inputs when prompted:

# enter the IP of your ISP to restrict access or enter 0.0.0.0/24 which allows any host to access the VM. Examples below
var.cidr_blocks
  Enter a value: 24.6.3.79/32

# enter your KMS keys. In my case it is testing_ami.pem
var.key_name
  Enter a value: testing_ami

# enter your VPC group
var.vpc_id
  Enter a value: vpc-8ff14ce4

