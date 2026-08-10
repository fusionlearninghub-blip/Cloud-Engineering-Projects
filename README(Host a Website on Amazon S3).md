<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://nextwork.ai/projects/aws-host-a-website-on-s3)

**Author:** Kingsley Osayande  
**Email:** kingsleyosayande2@gmail.com

---

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use S3 to host a static website. I'm doing this project to learn about ASW and cloud services and how they can be used to store objects in the cloud and even hostb websites

### Tools and concepts

Services I used were AWS. I created an Amazon s3 bucket where i hosted a static website. Key concepts I learnt include ACL, bucket policy, block public access, and permissions.

### Time, challenges, and wins

This project took me approximately 40 minutes. The most challenging part was writing the code for the bucket policy. It was most rewarding to host my first static website on amazon s3 bucket.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open up an Amazon s3 and then create a storage space inside to start storing websites.

### How long it took to create the bucket

Creating an S3 bucket took me less than 10 minutes. i learned about ACl and block public access

### Region selection

The Region I picked for my S3 bucket was N. Virginia because its the region thats closest to me. It lowers latency and cost.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two S3 buckets in the world can have the same name

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will download an HTML file that sets up your website, download a zip file of images for your website and also upload both files into your S3 bucket.

### Files I uploaded

I uploaded two files to my S3 bucket - they were index.html file and a folder of images and assets.

### How the files work together

Both files are necessary for this project as html gives the structure while the folder provides the contents.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make our website availaible public. This is static website hosting.

### Understanding website hosting

Website hosting means putting our website files on a web server designed to turn our files into a website page that people can visit.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went to the properties section and enable static website hosting, and i labelled index.html as the name of the document.

### Access Control Lists (ACLs)

An ACL is a set of rules that decides who can get access to a resource.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is an url that takes you to the website that you are hosting.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an 403 forbidden error the first time. The reason for this error was that objects in the object are public by default, even when switched off block public access

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make the website files in S3 publicly accessible because it will enable us to see our website live on the internet! 

### How I resolved the 403 error

To resolve this 403 Forbidden error, I checked both objects; index.html and the assets, then i clicked on actions and finally click on make public using acl.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to set up a bucket policy that stops people from deleting your index.html file. I'm doing this so that  test your policy and showcase your secret mission in your project documentation.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are a bit more advanced since you're using code, the level of control you get is much higher compared to using ACLs. The benefit of using bucket policies is you can now control more than just who can see/access an object, while ACLs are useful for updating the permissions for individual objects.

![Image](http://nextwork.ai/loving_white_lucky_whio/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy was created. I tested this by checking the index.html box and clicking delete and saw failed to delete object.

---

---
