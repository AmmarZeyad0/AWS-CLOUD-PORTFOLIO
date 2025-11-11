<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-ec2)

**Author:** ammar zeyad  
**Email:** ammarramadan38@gmail.com

---

## Launching VPC Resources

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is virtual private cloud it is useful because until now I had built it came along with the VPC

### How I used Amazon VPC in this project

I used Amazon VPC with AWS Wizard to build an entire resource map for VPC with a few minutes.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was, firstly, when I was building my own VPC it took some time and I felt a bit of Confusion moving between lists, but with AWS Wizrd make it way easier. 

### This project took me...

This project took me almost one hour to make sure I understood everything was new to me, and at the same time tried my best to apply the best practices.

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means that it's like you have your own physical system, and you can access it whenever you want to.

### SSH is a key method for directly accessing a VM

SSH traffic means Secure Shell, which is the protocol we use for this secure access to a remote machine. 

### To enable direct access, I set up key pairs

Key pairs is contain from two keys one it will be installed virtual in the instance and the other half you will store it localy in your device.

A private key's file format means... My private key's file format was (.pem) The .pem format, which stands for Privacy Enhanced Mail,

---

## Launching a public server

I had to change my EC2 instance's networking settings by going for the advanced setting before launching my instance from put it inside my own VPC, and connecting it to the public subnet that already has the route table, internet gateway connected to make my instance public.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because I tried my best to keep it as much as I can far away from the customer.

My private server's security group's source is my private subnets with creating a new security group which means I can also control the inbound traffic.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I used AWS Wizard to do everything from scratch i just gave him some info that is really important for me to build it correctly.

A VPC resource map is a visual diagram to build a VPC. 

My new VPC has a CIDR block of (10.0.0.0/24) It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because, until now, I have not made the VPC Peering, so it can easily connect without any problem. The opposite of the subnets; they always connect to each other most of the time.

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: 1 public subnets or 2 public subnets, This was because VPC wizard limits you to two public subnets to keep things straightforward. 

The set up page also offered to create NAT gateways, which are mostly it will be used for private subnets more than for the public ones. Basically, it's the best option you have to make your own resources connect directly to the public internet.  

![Image](http://learn.nextwork.org/curious_gray_jolly_orange/uploads/aws-networks-ec2_8ee57662)

---

---
