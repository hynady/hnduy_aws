---
title : "Summary"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

In this guide, we have gone through the steps from creating an S3 bucket to configuring and deleting a CloudFront Distribution. This is an important process to help you understand how to distribute content from S3 via CloudFront, as well as how to optimize web application performance.

1. **Create S3 Bucket:** We created a new bucket to store static content such as HTML, CSS, and images.
2. **Upload Content:** Files were uploaded to the bucket to be ready for distribution.
3. **Configure Access Permissions:** Set up a policy to allow public access to the files in the bucket.
4. **Create CloudFront Distribution:** We created a new Distribution, configured the origin as the S3 bucket to efficiently distribute content to users.
5. **Check and Verify:** Checked the CloudFront URL to ensure the content was successfully distributed.
6. **Delete CloudFront Distribution:** Finally, we took the necessary steps to disable and delete the Distribution when it was no longer needed.
7. **Clean Up Resources:** If the bucket is no longer needed, we deleted it to save costs.

This process not only helps you understand how to use S3 and CloudFront but also provides practical knowledge on how to manage AWS resources efficiently and cost-effectively.
> **Tip:** Always review the steps you have taken to ensure no steps are missed.