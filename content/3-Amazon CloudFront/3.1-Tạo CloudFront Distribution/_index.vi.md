---
title : "Tạo Distribution"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---


- Truy cập AWS CloudFront:
  - Từ [AWS Management Console](https://aws.amazon.com/console/), tìm kiếm và chọn "CloudFront".
![Truy cập AWS CloudFront](/image/done17.png)

- Nhấn vào "Create":
![Tạo Distribution](/image/done18.png)

- Chọn "Origin Domain Name", nhập URL S3 website của bạn (ví dụ: my-static-website-lab.s3.amazonaws.com).
- Chọn “Use website endpoint”
![Use website endpoint](/image/done19.png)
- Giữ các tùy chọn mặc định và nhấn "Create Distribution".
![Create Distribution](/image/done20.png)
