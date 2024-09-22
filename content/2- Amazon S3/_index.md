---
title : "Amazon S3"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---

### Amazon S3

### Theoretical Basis of Amazon S3

Amazon S3 (Simple Storage Service) is an object storage service provided by Amazon Web Services (AWS). S3 is designed to store and retrieve data with high reliability, security, and scalability. Below are the important concepts and features related to S3 in this lab:

#### 1. **Bucket**
   - **Bucket** is the most basic unit in Amazon S3, where objects are stored. Each bucket is uniquely named within an AWS region and can contain multiple objects such as files or other data.
   - In this lab, we will create a bucket to store static content (HTML, CSS, JavaScript) and use it as the origin for CloudFront to distribute content.

#### 2. **Object**
   - **Object** is the main component of data stored in S3, including file data and related metadata. Each object is uniquely identified by a **key** within a bucket.
   - In this lab, your content files (static website) will be stored as objects in the bucket.

#### 3. **Access Control**
   - S3 provides multiple ways to manage access to buckets and objects, including **Bucket Policies**, **IAM Roles**, and **Access Control Lists (ACLs)**.
   - In the lab, we will configure public access permissions for the objects in the bucket through a Bucket Policy to allow users to access the content via CloudFront.

#### 4. **Storage Features**
   - Amazon S3 offers various storage classes to optimize costs based on access frequency and performance requirements, including:
     - **S3 Standard**: For frequently accessed data.
     - **S3 Standard-IA**: For infrequently accessed data but requires quick retrieval.
     - **S3 Glacier**: For long-term storage with low cost.
   - In this lab, we will use **S3 Standard** as it is suitable for static content files that need to be quickly distributed via CloudFront.

#### 5. **S3 Static Website Hosting**
   - S3 allows you to host a static website directly from a bucket without a web server. HTML, CSS, and JavaScript files can be served as a static website. However, in this lab, we will not use this feature but instead use CloudFront to accelerate content distribution.
   
#### 6. **Integration with CloudFront**
   - Amazon CloudFront is a CDN (Content Delivery Network) that helps distribute content from sources like S3 to users with higher speed through edge locations worldwide.
   - In this lab, S3 will be used as the **Origin** for CloudFront, from which static content files will be distributed to users globally with the best performance.

#### 7. **Bucket Policy Configuration**
   - **Bucket Policy** allows you to control access for the entire bucket and all objects within it. This is particularly useful when you want to publicly share content in your bucket, such as static files that CloudFront will distribute.
   - We will create and apply a bucket policy to allow public access to the content without manually granting permissions for each file.

#### 8. **Security and Monitoring**
   - S3 supports data encryption at rest (server-side encryption) and in transit (SSL/TLS). You can enable encryption for objects to secure your data.
   - **S3 Logs** and **AWS CloudTrail** help track requests to the bucket, aiding in effective data management and security.

### Summary
Amazon S3 is a powerful and flexible storage tool that allows efficient storage and distribution of content. In this lab, you will learn how to use S3 as the origin for CloudFront to distribute static content globally. Configuring access permissions, bucket policies, and optimizing storage classes are crucial elements in the deployment process.

In this section, we will explore Amazon S3 and the steps to work with it.
- [Go to the guide to create an S3 Bucket](./2.1-create-s3-bucket/)
- [Go to the guide to upload content to the Bucket](./2.2-upload-content-to-bucket/)
- [Go to the guide to check](./2.4-check/)