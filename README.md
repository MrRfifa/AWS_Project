# AWS_Project
The objective of the project is to deploy a highly available (HA) web application on AWS, using HTML, CSS, PHP, and MySQL.

AWS Project

The objective of the project is to deploy a highly available (HA) web application on AWS. You can use any application with any language that interacts with a table in a MySQL database.

The application must be deployed on an EC2 instance. The necessary environment needs to be installed to run the application.

The diagram below presents the different components required for the AWS environment:

- Create a VPC (do not use the default one).
- Create 2 Public Subnets on 2 different Availability Zones (along with the necessary routing tables).
- Create 2 Private Subnets on 2 different Availability Zones (along with the necessary routing tables).
- Create an Internet Gateway.
- Create a Load Balancer (which should be in the 2 public subnets).
- Create an Autoscaling group for the EC2 instances (containing the web application) that should be in the Private Subnets.
- Add 2 NAT Gateways (in the public subnets) to allow EC2 instances to perform updates.
- Create a MYSQL database with RDS multi-AZ.
- Create 3 security groups: one for the load balancer, one for the EC2 instances.
- Add a bastion host for SSH access to the EC2 instances. Create the necessary security group for the bastion host (the bastion host is not shown in the diagram).
- Update the security groups of the EC2 instances to allow SSH access only via the bastion host.

![image](https://github.com/MrRfifa/AWS_Project/assets/101003527/cf4246ea-6fac-49a1-b44e-5df4b5a86500)
