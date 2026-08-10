<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://nextwork.ai/projects/aws-security-iam)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate using the AWS Identity and Access Management (IAM) service how to control who is authenticated (signed in) and authorized (has permissions) in your AWS account. I'm doing this project to learn how to launch an EC2 instance, then control who has access to it by creating some IAM policies and user groups.

### Tools and concepts

Services I used were EC2 instance, IAM user and IAM user group. Key concepts I learnt include creating an IAM user address to allow my interns to access the resources with logging in through the AWS management console.

### Project reflection

This project took me approximately 30 minutes. The most challenging part was logging in the IAM user address into another browser or using incognito. It was most rewarding to finally complete the task.

---

## Tags

### What I did in this step

In this step, I will launch an EC2 instance because i want to boost the computing power of nextwork company to match increased traffic to the website as we gear up for the upcoming holiday season.

### Understanding tags

Tags are like labels you can attach to AWS resources for organization. They helps us with identifying all resources with the same tag at once (they are useful filters when you're searching for something), cost allocation, and applying policies based on environment types. 

### My tag configuration

The tag I’ve used on my EC2 instances is called Env. The value I’ve assigned for my instances are production and development.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will create an IAM policy because it will give the interns access to the development instance.

### Understanding IAM policies

IAM Policies are rules that gives permissions to IAM users, groups, or roles, saying what they can or can't do on certain resources, and when those rules kick in.

### The policy I set up

For this project, I’ve set up a policy using the JSON

### Policy effect

I’ve created a policy that allows some actions (like starting, stopping, and describing EC2 instances) for instances tagged with "Env = development" while denying the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means allow or deny a certain action, actions that the policy allows or denies. , and Which resources does this policy apply to?

---

## My JSON Policy

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will simplify user login to my AWS account using an Account Alias because it makes it easier to remember and share your AWS console's login URL with others

### Understanding account aliases

An account alias is a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console.

### Setting up my account alias

Creating an account alias took me less than 3 minutes. Now, my new AWS console sign-in URL is https://nextwork-alias-kingsley.signin.aws.amazon.com/console

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will set up a dedicated IAM group for all NextWork interns and  a dedicated IAM user for my new intern so i can manage all interns' permissions from one place and they can have a way to log in.

### Understanding user groups

IAM user groups are the collections/folders of users for easier user management.

### Attaching policies to user groups

I attached the policy I created to this user group, which means interns can have access to the development instance but not to the production instance.

### Understanding IAM users

IAM users are the people that will get access to your resources/AWS account.

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is create an IAM user account, so he can get access to the resources with logging in with username and passwords.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed some of your dashboard panels are showing Access denied already. This was because the AWS console will treat you as someone that is starting from 0 again. Awesome for the new team member that you'll be giving this User to!

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will log into AWS using the intern's IAM user because i want to test the intern's access to my production and development instance.

### Testing policy actions

I tested my JSON IAM policy by stopping the production and development instances with the interns IAM user address. The policy holds true because the intern IAM user is unable to stop the instance for the production instance.

### Stopping the production instance

When I tried to stop the production instance with the IAM user address for the intern, it returned an error. This was because the set policy allows interns to only access development and not production.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance and it stopped. This was because the policy allows the interns IAM user to make changes to the development instance,

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to use the IAM Policy Simulator to test my users' permissions in a faster, more efficient way. I'm doing this because shutting ec2 instances could be disruprive for other engineers, so its best practive to run these test in a policy stimulator.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is useful for testing my users' permissions in a faster, more efficient way. 

### How I used the simulator

I set up a simulation for IAM policy. The results were denied. I had to adjust the instance field by adding development to indicate that you want to run the simulation for the instances with that tag.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-security-iam_069d8a621)

---

---
