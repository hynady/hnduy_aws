---
title : "Amazon CloudFront"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
### Cơ Sở Lý Thuyết Về Amazon CloudFront

Amazon CloudFront là dịch vụ mạng phân phối nội dung (Content Delivery Network - CDN) do Amazon Web Services cung cấp. CloudFront giúp tăng tốc phân phối nội dung (ví dụ: trang web, hình ảnh, video) cho người dùng trên toàn thế giới bằng cách sử dụng một mạng lưới các máy chủ phân phối (edge locations). Dưới đây là các khái niệm và tính năng quan trọng liên quan đến CloudFront trong lab này:

#### 1. **Content Delivery Network (CDN)**
   - **CDN** là mạng lưới các máy chủ phân phối nội dung, đặt tại nhiều vị trí địa lý khác nhau trên thế giới. Khi người dùng truy cập vào nội dung của bạn, CDN sẽ chuyển nội dung từ máy chủ gần nhất với họ, giúp giảm thời gian tải và cải thiện trải nghiệm người dùng.
   - Amazon CloudFront là một CDN cho phép bạn phân phối nội dung từ các nguồn (origin) như Amazon S3, EC2, hoặc thậm chí từ các máy chủ bên ngoài AWS.

#### 2. **Origin**
   - **Origin** là nguồn gốc nơi CloudFront lấy nội dung để phân phối. Các origin thường là Amazon S3 bucket, EC2 instance, hoặc một server HTTP khác.
   - Trong lab này, S3 bucket chứa nội dung tĩnh sẽ được sử dụng làm origin cho CloudFront để phân phối nội dung.

#### 3. **Edge Location**
   - **Edge Location** là các máy chủ đặt tại các vị trí địa lý khác nhau trên thế giới, nơi CloudFront lưu nội dung cache để phân phối nhanh chóng đến người dùng. Khi có yêu cầu từ người dùng, nội dung sẽ được trả về từ edge location gần nhất, giúp giảm độ trễ và tăng tốc độ tải.
   - Khi người dùng yêu cầu nội dung, CloudFront sẽ kiểm tra xem edge location gần nhất có bản sao (cached copy) của nội dung đó không. Nếu có, nội dung sẽ được phân phối từ cache. Nếu không, CloudFront sẽ lấy nội dung từ origin và lưu nó vào edge location cho các yêu cầu sau.

#### 4. **Distribution**
   - **Distribution** là khái niệm đại diện cho một tập hợp các quy tắc phân phối nội dung qua CloudFront. Bạn có thể tạo hai loại distribution:
     - **Web Distribution**: Dùng để phân phối nội dung web tĩnh và động, như HTML, CSS, JavaScript, hình ảnh và video.
     - **RTMP Distribution**: Dùng để truyền phát nội dung đa phương tiện (streaming) thông qua giao thức RTMP.
   - Trong lab này, chúng ta sẽ tạo **Web Distribution** để phân phối nội dung từ S3 bucket.

#### 5. **Cache Behavior**
   - **Cache Behavior** xác định cách CloudFront xử lý các yêu cầu và phân phối nội dung. Bạn có thể cấu hình các quy tắc cache behavior để kiểm soát cách CloudFront lưu trữ và phân phối các tệp nhất định, hoặc cách xử lý các phương thức HTTP (GET, POST, v.v.).
   - CloudFront cho phép bạn kiểm soát thời gian cache nội dung trong edge location (thông qua **TTL – Time to Live**), giúp tối ưu hóa việc phân phối nội dung.

#### 6. **Distribution Settings**
   - Khi tạo một CloudFront distribution, bạn có thể cấu hình nhiều thiết lập liên quan đến bảo mật và hiệu suất, bao gồm:
     - **Custom Domain Names (CNAMEs)**: Gán tên miền tùy chỉnh cho URL của CloudFront Distribution.
     - **SSL/TLS Certificates**: Cấu hình chứng chỉ SSL để mã hóa dữ liệu khi truyền tải giữa người dùng và CloudFront.
     - **Logging**: Kích hoạt tính năng logging để theo dõi các yêu cầu đến Distribution.
   - Những thiết lập này giúp tùy chỉnh cách CloudFront hoạt động, tối ưu bảo mật và theo dõi hiệu suất.

#### 7. **Invalidation**
   - **Invalidation** là cơ chế cho phép xóa nội dung được lưu trữ trong các edge location. Khi nội dung trong S3 được thay đổi hoặc cập nhật, CloudFront có thể phân phối phiên bản cũ từ cache. Để giải quyết điều này, bạn có thể yêu cầu invalidation để làm mới cache trên toàn bộ các edge location.
   - Invalidation giúp đảm bảo rằng người dùng luôn nhận được phiên bản mới nhất của nội dung.

#### 8. **Bảo Mật và Kiểm Soát Truy Cập**
   - CloudFront cung cấp nhiều tính năng bảo mật để kiểm soát quyền truy cập vào nội dung, bao gồm:
     - **Origin Access Control**: Kiểm soát truy cập từ CloudFront đến nguồn gốc (origin) như S3. Điều này giúp bảo vệ nội dung không bị truy cập trực tiếp từ S3.
     - **Geo-Restriction**: Giới hạn phân phối nội dung đến các quốc gia hoặc khu vực nhất định.
     - **Signed URLs và Signed Cookies**: Dùng để giới hạn thời gian hoặc quyền truy cập vào các tài nguyên cụ thể.
   - Trong lab này, chúng ta không cần cấu hình các tính năng bảo mật cao cấp, nhưng CloudFront vẫn hỗ trợ mã hóa SSL/TLS mặc định cho các kết nối.

#### 9. **Kết Hợp Với S3**
   - CloudFront hoạt động cùng S3 để phân phối nội dung tĩnh như hình ảnh, video, và các tệp khác với độ trễ thấp và tốc độ cao. Khi kết hợp với S3, CloudFront có thể cache nội dung tại các edge location, giúp giảm tải cho S3 và cải thiện thời gian phản hồi cho người dùng.

#### 10. **Tối Ưu Hóa Chi Phí**
   - Sử dụng CloudFront cùng với S3 không chỉ cải thiện hiệu suất mà còn giúp tối ưu hóa chi phí lưu trữ và truyền tải dữ liệu. Thay vì truy cập trực tiếp vào S3 mỗi khi có yêu cầu, CloudFront phân phối nội dung từ các edge location, giảm chi phí truyền tải và giúp giảm tải cho S3.
   
### Tóm Lại
Amazon CloudFront là một dịch vụ CDN mạnh mẽ giúp phân phối nội dung nhanh chóng và an toàn từ các nguồn như Amazon S3. Trong lab này, chúng ta sẽ học cách sử dụng CloudFront để tăng cường hiệu suất phân phối nội dung tĩnh từ S3, đồng thời cấu hình các tính năng cache và bảo mật cơ bản để cải thiện trải nghiệm người dùng toàn cầu.

## Trong phần này, chúng ta sẽ tìm hiểu về Amazon CloudFront và các bước để làm việc với nó.

- [Tạo CloudFront Distribution](./3.1-tạo-cloudfront-distribution/index.html)
- [Kiểm Tra CloudFront Distribution](./3.2-kiểm-tra-cloudfront-distribution/index.html)
