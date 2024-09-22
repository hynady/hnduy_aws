---
title : "Amazon S3"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---

### Amazon S3

### Cơ Sở Lý Thuyết Về Amazon S3

Amazon S3 (Simple Storage Service) là một dịch vụ lưu trữ đối tượng cung cấp bởi Amazon Web Services (AWS). S3 được thiết kế để lưu trữ và truy xuất dữ liệu với độ tin cậy cao, bảo mật và khả năng mở rộng. Dưới đây là các khái niệm và tính năng quan trọng liên quan đến S3 trong lab này:

#### 1. **Bucket**
   - **Bucket** là đơn vị cơ bản nhất trong Amazon S3, là nơi chứa các đối tượng (object) được lưu trữ. Mỗi bucket được đặt tên duy nhất trong một vùng AWS (region) và có thể chứa nhiều đối tượng như tệp tin hoặc dữ liệu khác.
   - Trong lab này, chúng ta sẽ tạo một bucket để lưu trữ nội dung tĩnh (HTML, CSS, JavaScript) và sử dụng nó làm nguồn (origin) cho CloudFront để phân phối nội dung.

#### 2. **Object**
   - **Object** là thành phần chính của dữ liệu lưu trữ trong S3, bao gồm dữ liệu tệp và siêu dữ liệu liên quan. Mỗi object được xác định duy nhất bằng một **key** trong bucket.
   - Trong lab này, các tệp nội dung của bạn (website tĩnh) sẽ được lưu trữ dưới dạng các object trong bucket.

#### 3. **Quyền Truy Cập (Access Control)**
   - S3 cung cấp nhiều cách để quản lý quyền truy cập đến bucket và object, bao gồm **Bucket Policies**, **IAM Roles**, và **Access Control Lists (ACLs)**.
   - Trong lab, chúng ta sẽ cấu hình quyền truy cập công khai cho các đối tượng trong bucket thông qua Bucket Policy để cho phép người dùng truy cập vào nội dung qua CloudFront.

#### 4. **Tính Năng Lưu Trữ**
   - Amazon S3 cung cấp nhiều lớp lưu trữ (storage classes) khác nhau để tối ưu chi phí dựa trên tần suất truy cập và yêu cầu hiệu suất, bao gồm:
     - **S3 Standard**: Dùng cho dữ liệu thường xuyên truy cập.
     - **S3 Standard-IA**: Dữ liệu ít được truy cập nhưng cần truy xuất nhanh.
     - **S3 Glacier**: Dùng cho lưu trữ lâu dài với chi phí thấp.
   - Trong lab này, chúng ta sẽ sử dụng **S3 Standard** vì đây là lớp lưu trữ phù hợp cho các tệp nội dung tĩnh cần phân phối nhanh chóng qua CloudFront.

#### 5. **S3 Static Website Hosting**
   - S3 cho phép bạn lưu trữ một website tĩnh trực tiếp từ bucket mà không cần máy chủ web. Các tệp HTML, CSS, và JavaScript có thể được phục vụ dưới dạng một trang web tĩnh. Tuy nhiên, trong lab này, chúng ta sẽ không sử dụng tính năng này, mà thay vào đó sử dụng CloudFront để tăng tốc phân phối nội dung.
   
#### 6. **Kết Nối Với CloudFront**
   - Amazon CloudFront là một CDN (Content Delivery Network) giúp phân phối nội dung từ các nguồn như S3 đến người dùng với tốc độ cao hơn nhờ vào các máy chủ phân phối (edge locations) trên toàn cầu.
   - Trong lab này, S3 sẽ được dùng làm **Origin** cho CloudFront, từ đó các tệp nội dung tĩnh được phân phối đến người dùng trên khắp thế giới với hiệu suất tốt nhất.

#### 7. **Cấu Hình Bucket Policy**
   - **Bucket Policy** cho phép bạn kiểm soát quyền truy cập cho toàn bộ bucket và tất cả các đối tượng trong bucket đó. Điều này đặc biệt hữu ích khi bạn muốn chia sẻ công khai các nội dung trong bucket của mình, chẳng hạn như các tệp tĩnh mà CloudFront sẽ phân phối.
   - Chúng ta sẽ tạo và áp dụng một chính sách bucket cho phép truy cập công khai tới nội dung mà không cần phải cấp quyền thủ công cho từng tệp.

#### 8. **Bảo Mật và Giám Sát**
   - S3 hỗ trợ mã hóa dữ liệu khi lưu trữ (server-side encryption) và khi truyền tải (SSL/TLS). Bạn có thể kích hoạt mã hóa cho c��c đối tượng để bảo mật dữ liệu của mình.
   - **S3 Logs** và **AWS CloudTrail** giúp theo dõi các yêu cầu đến bucket, giúp quản lý và bảo mật dữ liệu hiệu quả.

### Tóm Lại
Amazon S3 là một công cụ lưu trữ mạnh mẽ và linh hoạt cho phép lưu trữ và phân phối nội dung một cách hiệu quả. Trong lab này, bạn sẽ học cách sử dụng S3 như nguồn gốc (origin) cho CloudFront để phân phối nội dung tĩnh trên toàn cầu. Việc cấu hình quyền truy cập, bucket policy và tối ưu hóa các lớp lưu trữ là những yếu tố quan trọng trong quá trình triển khai.

Trong phần này, chúng ta sẽ tìm hiểu về Amazon S3 và các bước để làm việc với nó.
- [Đi đến hướng dẫn tạo S3 Bucket](./2.1-tạo-s3-bucket/)
- [Đi đến hướng dẫn tải nội dung lên Bucket](./2.2-tải-nội-dung-lên-bucket/)
- [Đi đến hướng dẫn kiểm tra](./2.4-kiểm-tra/)