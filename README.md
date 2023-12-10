# Configuring-ALB-among-two-VPC

## Important Terms

ELB= Elastic load balancer is basically used for efficiently manage traffic with high avaibility.

there are three type of ELB available in AWS

1-Application Load Balancer 

2-Network Load Balancer 

3-Gatway Load Balancer

And one more outdated (Classic Load Balancer)

Load balancer distribute loads using

1.Listner

2.Target Groups

3.Target

## Now start...->

First of all you have to create two VPC in same region.

(Let's assume Vpc1 have 11.0.0.0/16 cidr range,

vpc2 have 12.0.0.0/16 cidr range)

Than you have to create atleast 2 subnet one public and one private in two az

Now attach internet gatway in both VPCs for going to public

Add route for internet access.

Configure VPC Peering connection so both vpcs able to communicate.

Now launch Ec2 instances with Amazon Linux Ami (u can choose other also) one for each subnet, inside VPC,

Note down the private ip of each instance so we can check our LB working or not...😀

Now login to ur instance using istance connect and install apache for web server.

and create a html file and write "Hello World!" or whatever you want.🤗

Now configure the ALB 






