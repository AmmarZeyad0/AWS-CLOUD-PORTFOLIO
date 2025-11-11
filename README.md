<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-security)

**Author:** ammar zeyad  
**Email:** ammarramadan38@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a service that provisions a logically isolated virtual network within the AWS Cloud

### How I used Amazon VPC in this project

I used Amazon VPC to create a secure, isolated foundational network layer on AWS, defining its boundaries with a specific CIDR block (e.g., $10.0.0.0/16$). Within this VPC, I created Subnets, which are essential for organizing resources across Availability Zones. The VPC was then connected to the public internet by attaching an Internet Gateway (IGW) and configuring the Route Table of the Public Subnet to route all external traffic ($\mathbf{0.0.0.0/0}$) to that IGW. This process successfully established the network backbone required for deploying and isolating cloud resources

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was a little messy about the different roles between Network ACLs and the Security Groups.

### This project took me...

This project took me almost 30min to be build successfully.

---

## Route tables

Route tables are sets of rules that can be modified as I need it for my subnets to make them private or public to control the traffic routes.

The primary reason for a Route Table is that it provides the directions (or "routes") that instruct network traffic on how to exit the VPC and reach the public Internet.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

Destination: This is the IP address range (CIDR) that the network traffic is trying to reach.

Target: This is the next network device or gateway (like an IGW, NAT Gateway, or local) that the traffic must be sent to to reach that destination."

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of (0.0.0.0) > and targeted the IGW to be public and had also (10.0.0.0./16) that targeted the local to let my device have access to the internet.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are responsible for checking who comes in and out.

### Inbound vs Outbound rules

Inbound rules control the data that can enter the resources in your security group, I  configured an inbound rule that all HTTP from Anywhere-IPv4.

Outbound rules control the data that your resources can send out. By default, my security group's outbound rule is All traffic to make it accessible for public internet.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs act like a firewall at the subnet level and it's statless, secondary layer of protection.

### Security groups vs. network ACLs

"The main difference is the scope and the statefulness. Security Groups are stateful firewalls that apply to the instance level (primary layer), meaning they automatically allow reply traffic. Network ACLs are stateless firewalls applied at the subnet level (secondary layer), meaning you must explicitly define both inbound and outbound rules for traffic and its reply

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

A default Network ACL starts as a fully open firewall.

The default rules for both Inbound and Outbound traffic are set to Allow All (often seen as Rule 100).

A custom Network ACL starts as a fully closed firewall.

It has an implicit Deny All rule for both Inbound and Outbound traffic.

This means you must explicitly add 'Allow' rules for any traffic you want to permit to enter or leave the Subnet. It's a security-first approach where you only open the specific ports you need.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

---

---
