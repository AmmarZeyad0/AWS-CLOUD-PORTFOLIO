<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-private)

**Author:** ammar zeyad  
**Email:** ammarramadan38@gmail.com

---

## Creating a Private Subnet

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC (Virtual Private Cloud) is your own logically isolated private network within the AWS cloud.

It is useful for two main reasons:

Security and Isolation: It completely separates your resources from other AWS customers, providing a secure, dedicated environment for your applications and data.

Network Control: It gives you total power to design your network architecture—setting your own IP addresses, creating public subnets (for internet access), and secure private subnets (for databases).

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to host my private subnets and the private route table as well to keep everything working smoothly.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how I should remove the route to an internet gateway, and it wasn't that enough to prevent traffic from the internet.

### This project took me...

This project took me 15 minutes to be done successfully.

---

## Private vs Public Subnets

The difference between public and private subnets is that the private is connected to the internet, but it is kept isolated from being accessed by public users on the internet.

Having private subnets is useful, for example, you are hosting a website in the cloud and you want the user to interact only with the content and prevent them from accessing the data you have and keep it safe.

My private and public subnets cannot have the same CIDER addresse.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with NextWork route table is the default route table for my entire VPC. Subnets that aren't associated with another route table automatically use NextWork route table with IGW to be public for the user on the internet

I had to set up a new route table because I want my new private subnet that I'd created to be isolated from being publicly accessible by the users, so I decided to set up a new private route table for it.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows the inbound traffic to pass inside for communications between my services only, and one outbound rule that denies every traffic.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with a default network ACL set up for every VPC from AWS, and it's not working with my private subnet because it has a route to be access from all traffic (100)

I set up a dedicated network ACL for my private subnet because I want it to be isolated from being accessed on the internet.

My new network ACL has two simple rules - (Deny all traffic from all as inbound rule) & (Deny all traffic from all as outbound rule).

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-private_1ed2cb07)

---

---
