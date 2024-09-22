---
title : "Overview"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
## 1. Lab Objectives

- Understand how to host a static website on S3.
- Understand how to use CloudFront to optimize the website.
- Use free services or incur no costs.

## 2. Basic Knowledge

- **Amazon S3 (Simple Storage Service):**
  - Amazon S3 is an object storage service that provides the ability to store data files in "buckets". S3 is very popular for storing large data or static websites (HTML, CSS, JS). Static websites do not require backend processing servers but only have fixed content.
- **Amazon CloudFront:**
  - CloudFront is AWS's content delivery network (CDN) service, which helps improve website load performance by caching static content and distributing it from locations closest to the end users.
- **Cost:**
  - S3 provides 5GB free in the free tier.
  - CloudFront has a free tier for 1TB of data transfer each month for the first 12 months.

## 3. Lab Requirements

- AWS account with free tier.
- A simple static website (just a few basic HTML, CSS, and JS files).

## 4. Navigation

- [Introduction](./index.html)
- [Create S3 Bucket](../2--amazon-s3/2.1-create-s3-bucket/index.html)
- [Upload Content to Bucket](../2--amazon-s3/2.2-upload-content-to-bucket/index.html)
- [Configure Bucket for Static Website](../2--amazon-s3/2.3-configure-bucket-for-static-website/index.html)
- [Check](../2--amazon-s3/2.4-check/index.html)
- [Create CloudFront Distribution](../3-amazon-cloudfront/3.1-create-cloudfront-distribution/index.html)
- [Check CloudFront Distribution](../3-amazon-cloudfront/3.2-check-cloudfront-distribution/index.html)
- [Delete CloudFront Distribution](../4-delete-and-clean-up-resources/4.1-delete-cloudfront-distribution/index.html)
- [Delete S3 Bucket](../4-delete-and-clean-up-resources/4.2-delete-s3-bucket/index.html)
- [Check Successful Cleanup](../4-delete-and-clean-up-resources/4.3-check-successful-cleanup/index.html)
- [Summary](../5-summary/index.html)

> **Note:** This is an introduction to the steps involved in the project.