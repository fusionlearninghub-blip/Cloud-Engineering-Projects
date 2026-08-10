<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-vpc)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate how to build a Virtual Private Cloud. I'm doing this project to learn how to create an Amazon VPC, a public subnet, and an internet gateway.

### What is Amazon VPC?

### Personal reflection

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create an Amazon VPC because it gives me an isolated, private network in AWS where I control exactly how my resources (like EC2 instances) can communicate with each other and with the internet.

### How VPCs work

VPCs are the overall private network space in AWS that you divide into subnets — and subnets are what actually hold your resources. You also get control over resources in a VPC, so you can organize how they communicate and integrate with each other without the public internet.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because without a default VPC, i would not be able to launch resources (e.g. EC2 instances) and connect services together from Day 1 of using AWS.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is  (which stands for Classless Inter-Domain Routing) is a way to assign a whole block of IP addresses, kind of like creating a zone/area in a city.

---

## Subnets

### What I did in this step

In this step, I will because create a subnet under my Virtual Private Cloud(VPC). Subnets are logical divisions of an IP network. They allow you to break a large network into smaller, more manageable segments. This improves security, performance, and organization by isolating traffic and resources within specific parts of your network.

### Creating and configuring subnets

Subnets are like different neighborhoods inside your city. You use subnets to group resources with similar access rules and restrictions. Some subnets might be public areas that all resources can access (public subnets) while others are private areas with limited access (private subnets). There are already subnets existing in my account, one for every Availability Zone.

### Public vs private subnets

The difference between public and private subnets are: a public subnet is connected to the internet. Resources inside a public subnet can communicate with external networks.
A private subnet does not have direct internet access. You'd use it for internal resources that don’t need to be publicly accessible.
 For a subnet to be considered public, it has to be connected to an Internet Gateway.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses. This setting makes sure the subnet hav access to the internet or be accessible from the internet so that any EC2 instance launched in that subnet will instantly get a public IP address so you won't have to create one manually.

---

## Internet gateways

### What I did in this step

In this step, I will connect my Virtual Private Cloud (VPC) to the internet gateway (IGW);  so my resources can communicate beyond your private space.

### Setting up internet gateways

Internet gateways is like a bridge that links the Virtual Private Cloud (VPC) to the public internet, so your resources can communicate beyond your private space.

Attaching an internet gateway to a VPC means resources in your VPC can now access the internet. If I missed this step, the resources in my vpc will not be connected to the internet.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will Launch a VPC in Seconds with AWS CloudShell because i want to report back on whether it was a faster, more efficient way to do this project.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell; a space for you to run code. CLI (command line interface) is a software that lets you create, delete and update AWS resources with commands instead of clicking through your console.

### Debugging my setup

To set up a VPC or a subnet, you can use the command line interface. Make sure to avoid errors by including CIDR block to your create-subnet command.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is that it provides the speed and versatility that professionals need for complex tasks. An advantage of using the Console is that its fantastic for learning and having a visual guide. Overall, I preferred using the Commands.

---

---
