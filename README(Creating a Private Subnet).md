<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-private)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

## Creating a Private Subnet

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a logically isolated, private section of the AWS cloud where you can launch and organize your own AWS resources — like EC2 instances and databases — inside a network whose IP range, subnets, and routing you define yourself. It is useful because it provides security and structure for your resources; public and private subnets.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create a private subnet.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is that custom, private Network ACL needs to be created for extra security even if the private subnet does not have an Internet Gateway.

### This project took me...

This project took me about 45 minutes.

---

## Private vs Public Subnets

The difference between public and private subnets is that a public subnet is connected to the client i.e user through the internet gateway while a private subnet is not connected to the client i.e user.

Having private subnets are useful because it keeps resources, informations or database that you dont want to share private.

My private and public subnets cannot have the same CIDR block.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with NextWork route table.

I had to set up a new route table because the public subnet and private subnet cannot use the same route table. If used, the private subnet becomes public.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows traffic within the VPC itself — it has a local route of 10.0.0.0/16 → local covering communication between resources inside the VPC, but no route to an Internet Gateway (0.0.0.0/0), so it has no path for traffic to reach or come from the public internet.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with VPC's defaults network ACL.

I set up a dedicated network ACL for my private subnet because the default NACL allows all traffic in and out by default, which doesn't give me any real subnet-level security — I need a custom NACL to explicitly control (and restrict) what traffic is allowed into and out of my private subnet.

My new network ACL has two simple rules - deny all

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-private_1ed2cb07)

---

---
