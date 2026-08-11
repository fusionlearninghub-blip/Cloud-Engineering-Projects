<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-ec2)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

## Launching VPC Resources

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a logically isolated, private section of the AWS cloud where you can launch and organize your own AWS resources — like EC2 instances, databases — inside a network whose IP address range, subnets, and routing you fully define and control. It is useful because it lets you design your cloud network exactly the way you need it: separating resources into public subnets (internet-facing) and private subnets (shielded from direct internet access), controlling traffic in and out with security groups and network ACLs, and connecting components securely — all while staying isolated from every other AWS customer, so your resources are only reachable in the ways you explicitly allow.

### How I used Amazon VPC in this project

I used Amazon VPC to build a fully custom, secure network from scratch — defining my own IP ranges, separating public and private instances, controlling traffic with route tables/security groups/NACLs, and connecting two EC2 instances within that isolated environment.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was that having more private subnets is cool and secure for organizing resources (database) while its better to have fewer public subnets to make it manageable to connect to the internet through the internet gateway.

### This project took me...

This project took me about 80 minutes to complete.

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means logging into and managing the operating system or software of the machine as if you were using it in front of you, but over the internet.

### SSH is a key method for directly accessing a VM

SSH traffic means Once SSH has established a secure connection between you and the EC2 instance, all data transmitted (including your commands and the responses from the instance) is encrypted. 

### To enable direct access, I set up key pairs

A key pair is a set of two cryptographic keys — a public key AWS stores on your instance, and a private key you keep — used to securely authenticate and log in to your EC2 instance instead of using a password. Key pairs help engineers directly access their virtual machines, like EC2 instances.


A private key's file format means Privacy Enhanced Mail; the go-to format for managing cryptographic keys because it is supported by many different types of servers e.g. EC2 instances! My private key's file format was .pem.

---

## Launching a public server

Start your response with 'I had to change my EC2 instance's networking settings by; 
- Selecting 'edit' at the right hand corner
- Selecting NextWork VPC from the drop-down in the VPC list, 
- Selecting my public subnet.
For the Firewall (security groups), we've already created the security group for your public subnet's resources. 
- I Selected the existing security group.
- I selected NextWork Public Security Group.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because this restricts access to a much smaller group of trusted resources, rather than allowing potentially any IP address on the internet (0.0.0.0/0) to access your instance. 

My private server's security group's source is Nextwork Public Security Group which means restricting access to a much smaller group of trusted resources

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I selected VPC and more. I had options on what to do or customize in my Amazon VPC all in one page. It was a lot faster that moving from page to page.

A VPC resource map is a map that helps you understand how different components in your setup are connected and interact with each other. This makes it easier to design, manage, and troubleshoot your architecture because you can see everything at a glance, rather than sifting through lists and configurations.

My new VPC has a CIDR block of 10.0.0.0/16. It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because VPC are isolated and do not share resources or communicate with each other except by VPC peering.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: us-east-2a and us-east-2b. This was because AWS only let me choose from the Availability Zones that actually exist within the Region I selected for my VPC — and different Regions have different numbers of AZs available.

NAT Gateways are a managed AWS service that lets instances in a private subnet reach the internet (updates or patches) without being directly reachable from the internet.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-ec2_8ee57662)

---

---
