---
title : "Delete CloudFront Distribution"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

- Access CloudFront:
  - In the [AWS Management Console](https://aws.amazon.com/console/), search for "CloudFront" and open the service.
- Select the Distribution to delete:
  - Find the Distribution you created.
  - Select that Distribution and click "Disable". This will stop CloudFront from distributing content.
![Delete CloudFront Distribution](/image/done23.png)

- Delete the Distribution:
  - Once the Distribution has changed to "Disabled" status, select it again and click "Delete".
  - Confirm the deletion.
- Note: The process of deleting a CloudFront Distribution may take a few minutes to complete.
![Delete Distribution](/image/done24.png)
![Result](/image/done25.png)