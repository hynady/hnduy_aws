---
title : "Tổng quan"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
## 1. Mục tiêu của Lab

- Hiểu cách lưu trữ một website tĩnh trên S3.
- Hiểu cách sử dụng CloudFront để tối ưu hóa website.
- Sử dụng dịch vụ miễn phí hoặc không phát sinh chi phí.

## 2. Kiến thức cơ bản

- **Amazon S3 (Simple Storage Service):**
  - Amazon S3 là dịch vụ lưu trữ đối tượng cung cấp khả năng lưu trữ tệp dữ liệu trong các "buckets". S3 rất phổ biến cho việc lưu trữ dữ liệu lớn hoặc các trang web tĩnh (HTML, CSS, JS). Website tĩnh không yêu cầu máy chủ xử lý phía sau mà chỉ có nội dung cố định.
- **Amazon CloudFront:**
  - CloudFront là dịch vụ phân phối nội dung (CDN) của AWS, giúp cải thiện hiệu suất tải trang web bằng cách cache nội dung tĩnh và phân phối từ các địa điểm gần nhất với người dùng cuối.
- **Chi phí:**
  - S3 cung cấp 5GB miễn phí trong tầng miễn phí.
  - CloudFront có tầng miễn phí cho 1TB dữ liệu truyền tải mỗi tháng trong 12 tháng đầu.

## 3. Yêu cầu Lab

- Tài khoản AWS với tầng miễn phí.
- Một website tĩnh đơn giản (chỉ cần vài file HTML, CSS và JS cơ bản).

## 4. Điều hướng

- [Giới thiệu](./index.html)
- [Tạo S3 Bucket](../2--amazon-s3/2.1-tạo-s3-bucket/index.html)
- [Tải Nội Dung Lên Bucket](../2--amazon-s3/2.2-tải-nội-dung-lên-bucket/index.html)
- [Cấu Hình Bucket Cho Website Tĩnh](../2--amazon-s3/2.3-cấu-hình-bucket-cho-website-tĩnh/index.html)
- [Kiểm Tra](../2--amazon-s3/2.4-kiểm-tra/index.html)
- [Tạo CloudFront Distribution](../3-amazon-cloudfront/3.1-tạo-cloudfront-distribution/index.html)
- [Kiểm Tra CloudFront Distribution](../3-amazon-cloudfront/3.2-kiểm-tra-cloudfront-distribution/index.html)
- [Xóa CloudFront Distribution](../4-xóa-và-dọn-dẹp-tài-nguyên/4.1-xóa-cloudfront-distribution/index.html)
- [Xóa S3 Bucket](../4-xóa-và-dọn-dẹp-tài-nguyên/4.2-xóa-s3-bucket/index.html)
- [Kiểm Tra Dọn Dẹp Thành Công](../4-xóa-và-dọn-dẹp-tài-nguyên/4.3--kiểm-tra-dọn-dẹp-thành-công/index.html)
- [Tổng Kết](../5-tổng-kết/index.html)

> **Note:** Đây là phần giới thiệu về các bước thực hiện trong dự án.