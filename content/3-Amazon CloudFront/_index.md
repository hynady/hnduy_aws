---
title : "Amazon CloudFront"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
### Theoretical Basis of Amazon CloudFront

Amazon CloudFront is a content delivery network (CDN) service provided by Amazon Web Services. CloudFront accelerates the distribution of content (e.g., websites, images, videos) to users worldwide by using a network of edge locations. Below are the important concepts and features related to CloudFront in this lab:

#### 1. **Content Delivery Network (CDN)**
   - **CDN** is a network of servers located in various geographical locations worldwide. When users access your content, the CDN delivers the content from the server closest to them, reducing load times and improving user experience.
   - Amazon CloudFront is a CDN that allows you to distribute content from origins such as Amazon S3, EC2, or even external servers.

#### 2. **Origin**
   - **Origin** is the source from which CloudFront fetches content to distribute. Origins are typically Amazon S3 buckets, EC2 instances, or other HTTP servers.
   - In this lab, the S3 bucket containing static content will be used as the origin for CloudFront to distribute content.

#### 3. **Edge Location**
   - **Edge Location** are servers located in various geographical locations worldwide where CloudFront caches content for quick distribution to users. When a user requests content, it is delivered from the nearest edge location, reducing latency and speeding up load times.
   - When users request content, CloudFront checks if the nearest edge location has a cached copy of the content. If it does, the content is delivered from the cache. If not, CloudFront fetches the content from the origin and caches it at the edge location for future requests.

#### 4. **Distribution**
   - **Distribution** represents a set of rules for distributing content via CloudFront. You can create two types of distributions:
     - **Web Distribution**: Used for distributing static and dynamic web content, such as HTML, CSS, JavaScript, images, and videos.
     - **RTMP Distribution**: Used for streaming media content via the RTMP protocol.
   - In this lab, we will create a **Web Distribution** to distribute content from the S3 bucket.

#### 5. **Cache Behavior**
   - **Cache Behavior** defines how CloudFront handles requests and distributes content. You can configure cache behavior rules to control how CloudFront caches and distributes specific files or handles HTTP methods (GET, POST, etc.).
   - CloudFront allows you to control the cache duration in edge locations (through **TTL – Time to Live**), optimizing content distribution.

#### 6. **Distribution Settings**
   - When creating a CloudFront distribution, you can configure various settings related to security and performance, including:
     - **Custom Domain Names (CNAMEs)**: Assign custom domain names to the CloudFront Distribution URL.
     - **SSL/TLS Certificates**: Configure SSL certificates to encrypt data during transmission between users and CloudFront.
     - **Logging**: Enable logging to track requests to the Distribution.
   - These settings help customize CloudFront's operation, optimize security, and monitor performance.

#### 7. **Invalidation**
   - **Invalidation** is a mechanism that allows you to remove cached content from edge locations. When content in S3 is changed or updated, CloudFront may distribute the old version from the cache. To resolve this, you can request invalidation to refresh the cache across all edge locations.
   - Invalidation ensures that users always receive the latest version of the content.

#### 8. **Security and Access Control**
   - CloudFront provides various security features to control access to content, including:
     - **Origin Access Control**: Controls access from CloudFront to the origin, such as S3. This helps protect content from being accessed directly from S3.
     - **Geo-Restriction**: Limits content distribution to specific countries or regions.
     - **Signed URLs and Signed Cookies**: Used to restrict time or access to specific resources.
   - In this lab, we do not need to configure advanced security features, but CloudFront still supports default SSL/TLS encryption for connections.

#### 9. **Integration with S3**
   - CloudFront works with S3 to distribute static content such as images, videos, and other files with low latency and high speed. When combined with S3, CloudFront can cache content at edge locations, reducing the load on S3 and improving response times for users.

#### 10. **Cost Optimization**
   - Using CloudFront with S3 not only improves performance but also helps optimize storage and data transfer costs. Instead of accessing S3 directly for each request, CloudFront distributes content from edge locations, reducing transfer costs and easing the load on S3.
   
### Summary
Amazon CloudFront is a powerful CDN service that helps distribute content quickly and securely from sources like Amazon S3. In this lab, we will learn how to use CloudFront to enhance the performance of distributing static content from S3, while configuring basic caching and security features to improve the global user experience.

## In this section, we will explore Amazon CloudFront and the steps to work with it.

- [Create CloudFront Distribution](./3.1-create-cloudfront-distribution/index.html)
- [Check CloudFront Distribution](./3.2-check-cloudfront-distribution/index.html)