<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-security)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a logically isolated section of the AWS cloud where you can launch AWS resources — like EC2 instances, databases, and load balancers — inside a network that you fully define and control.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create a route table, security group and a Network ACL.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was the use of AWS Global view to find and manage your EC2 and VPC resources across all AWS Regions from a single dashboard.

### This project took me...

This project took me about 40 minutes.

---

## Route tables

a route table is a table of rules, called routes, that decide where the data in your network should go.

Routes tables are needed to make a subnet public because it has routes that directs the internet bound traffic to the Internet Gateway.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

Routes are defined by their destination and target, which mean Destination as The IP address range that traffic wants to reach and Target as the road or path that the traffic will have to take to get to its destination.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of igw-0e09adbae1c56ab0c.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are responsible for checking who comes in and out. They have strict rules about what kind of traffic can enter or leave the resource based on its IP address, protocols and port numbers.

### Inbound vs Outbound rules

Inbound rules are used to control datra that enters the resources in your security group. I  configured an inbound rule that allows users to access your public website.

Outbound rules are rules that control data that your resources can send out. By default, my security group's outbound rule is already allowed by AWS . So unless you specify otherwise, any resource associated with the security group can access and send data to any IP address - whether it's in your VPC, other VPCs (if you have the right permissions) and on the public internet!

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are like as traffic cops stationed at every entry and exit point of your subnet, checking each data packet against a table of ACL rules before allowing them through

### Security groups vs. network ACLs

The difference between a security group and a network ACL is that network ACLs work at the subnet level, while security groups work at the resource level. 

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will allow all inbound and outbound traffic. 

In contrast, a custom ACL’s inbound and outbound rules are automatically set to deny all inbound and outbound traffic until you add rules about the kind of traffic you'll allow.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

I created additional Vpc, internet gateway and security group. Instead of my usual region, I used Ohio
us-east-2. Teams would use multiple regions to Improve latency for their end users, which means apps run faster because resources are physically closer to the users' location and to Protect themselves from natural disasters and other risks - if one Region experiences an outage, other Regions can maintain operations.

EC2 Global View is a tool where you can find and manage your EC2 and VPC resources across all AWS Regions from a single dashboard. I could even narrow down my search by typing the name of the region. Without EC2 Global View, you'd have to switch between Regions to track your resources.

Now that I've learnt about EC2 Global View, I'd use it again to find and manage your EC2 and VPC resources across all AWS Regions from a single dashboard.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-security_b03ea6162)

---

---
