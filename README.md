# ![AWSLogo](https://github.com/Nikhil-Singh25/Images_logos/blob/main/pngwing.com.png) + ![Terraform Logo](https://github.com/Nikhil-Singh25/Images_logos/blob/main/pngwing.com%20(1).png)     <br/>  AWS-Terraform Stack  
This is a Terraform script that creates an AWS Virtual Private Cloud (VPC) along with various resources such as an internet gateway, a route table, a subnet, a security group, a network interface, an elastic IP address, and an EC2 instance with Apache2 installed.

## Prerequisites

Before running this Terraform script, you need to have the following:

* An AWS account with valid credentials
* Terraform installed on your local machine

## Usage
   * Clone this repository onto your local machine.
   * In the project directory, run terraform init to initialize the Terraform configuration.
   * Run terraform plan to see the resources that will be created.
   * Run terraform apply to create the resources.
   * After the resources are created, you can access the EC2 instance by navigating to its public IP address in a web browser.

## Resource created
   * A VPC with specified CIDR block
   * An internet gateway attached to VPC
   * A route table attached to the VPC with a default route to the internet gateway
   * A subnet within the VPC with a specified CIDR block
   * A security group attached to the VPC with inbound rules allowing traffic on ports 80, 443, and 22
   * A network interface attached to the subnet with a specified private IP address
   * An elastic IP address attached to the network interface
   * An EC2 instance with Apache2 installed running in the subnet and attached to the network interface

## Variables 
   This Terraform script uses the following variables:
   * `CIDR-Production-VPC`: The CIDR block for the VPC. Default: `10.192.0.0/16`
   * `CIDR-Production-subnet`: The CIDR block for the subnet. Default: `10.192.10.0/24`
   * `ingress_ports`: The list of inbound ports to allow traffic on. Default: `[443, 80, 22]`
## Authors

-This terraform script was created and maintained by [@Nikhil_Singh](https://github.com/Nikhil-Singh25)


## License

* This Terraform script is Licensed under MIT  License.See `LISCENCE` for more information

