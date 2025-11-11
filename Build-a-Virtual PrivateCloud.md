<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** ammar zeyad  
**Email:** ammarramadan38@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a virtual private cloud, and it is useful because you can put your resources in an isolated place on the internet by having a (public, private) subnet.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to get a handy project to know how exactly things work in the VPC area.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how easy to launch an VPC with subnets,

### This project took me...

This project took me almost 30 minutes to make everything work and start from scratch.

---

## Virtual Private Clouds (VPCs)

VPCs enable you to make resources private, giving you control over resources within a VPC. You can organize how these resources communicate and integrate, ensuring they remain private.

There was already a default VPC in my account ever since my AWS account was created. This is because AWS created this one by default to make other services work without worrying about how to create VPC  from the beginning.

To set up my VPC, I had to define an IPv4 CIDR block, which stands for (Classless Inter-Domain Routing) is a way to assign a whole block of IP addresses, kind of like creating a zone/area in a city.



![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-vpc_2facf927)

---

## Subnets

Subnets are of two types: the first one is called a public subnet, where resources can be accessed publicly, the second one is called a private subnet, where you keep the data private from the public, and both subnets allocated inside the VPC.

Once I created my subnet, I enabled auto-assign public IPv4 addresses, This setting makes sure every EC2 instance i will launched in that subnet will instantly get a public IP assress so that I won't have to create one manually.

The difference between public and private subnets is that public can communicate with external networks, but private you'd used it for internal resources. For a subnet to be considered public, it has to be attached to an Internet Gateway.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-vpc_157c4219)

---

## Internet gateways

Internet gateways are key to making applications available on the Internet. By attaching an internet gateway, an instance can access the internet and be accessible to external users.

Attaching an internet gateway to a VPC means resources in my VPC can now access the internet. 

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

---

---
