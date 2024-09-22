---
title : "Tổng kết"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

Trong hướng dẫn này, chúng ta đã thực hiện các bước từ việc tạo một S3 bucket cho đến việc cấu hình và xóa một CloudFront Distribution. Đây là quy trình quan trọng giúp bạn hiểu cách phân phối nội dung từ S3 qua CloudFront, đồng thời cũng là cách để tối ưu hóa hiệu suất ứng dụng web.

1. **Tạo S3 Bucket:** Chúng ta đã tạo một bucket mới để lưu trữ nội dung tĩnh như HTML, CSS, và hình ảnh.
2. **Tải Nội Dung Lên:** Các tệp đã được tải lên bucket để sẵn sàng cho việc phân phối.
3. **Cấu Hình Quyền Truy Cập:** Thiết lập chính sách cho phép truy cập công khai vào các tệp trong bucket.
4. **Tạo CloudFront Distribution:** Chúng ta đã tạo một Distribution mới, cấu hình origin là bucket S3 để phân phối nội dung hiệu quả đến người dùng.
5. **Kiểm Tra và Xác Nhận:** Kiểm tra URL CloudFront để đảm bảo nội dung đã được phân phối thành công.
6. **Xóa CloudFront Distribution:** Cuối cùng, chúng ta đã thực hiện các bước cần thiết để vô hiệu hóa và xóa Distribution khi không còn cần thiết.
7. **Dọn Dẹp Tài Nguyên:** Nếu không cần sử dụng bucket nữa, chúng ta đã xóa nó để tiết kiệm chi phí.

Quy trình này không chỉ giúp bạn hiểu rõ cách sử dụng S3 và CloudFront mà còn cung cấp kiến thức thực tiễn về cách quản lý tài nguyên trên AWS một cách hiệu quả và tiết kiệm.
> **Tip:** Hãy luôn kiểm tra lại các bước đã thực hiện để đảm bảo không bỏ sót bất kỳ bước nào.