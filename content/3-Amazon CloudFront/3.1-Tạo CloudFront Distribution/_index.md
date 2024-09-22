---
title : "Create Distribution"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---

- Access AWS CloudFront:
  - From the [AWS Management Console](https://aws.amazon.com/console/), search for and select "CloudFront".
![Access AWS CloudFront](/image/done17.png)

- Click on "Create":
![Create Distribution](/image/done18.png)

- Select "Origin Domain Name", enter your S3 website URL (e.g., my-static-website-lab.s3.amazonaws.com).
- Select “Use website endpoint”
![Use website endpoint](/image/done19.png)
- Keep the default options and click "Create Distribution".
![Create Distribution](/image/done20.png)