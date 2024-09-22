---
title : "Xóa CloudFront Distribution"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---


- Truy cập CloudFront:
  - Trong [AWS Management Console](https://aws.amazon.com/console/), tìm kiếm "CloudFront" và mở dịch vụ này.
- Chọn Distribution cần xóa:
  - Tìm Distribution mà bạn đã tạo.
  - Chọn Distribution đó và nhấn "Disable". Việc này sẽ ngăn CloudFront tiếp tục phân phối nội dung.
![Xóa CloudFront Distribution](/image/done23.png)

- Xóa Distribution:
  - Sau khi Distribution đã chuyển sang trạng thái "Disabled", chọn nó lại và nhấn "Delete".
  - Xác nhận xóa.
- Lưu ý: Quá trình xóa CloudFront Distribution có thể mất vài phút để hoàn tất.
![Xóa Distribution](/image/done24.png)
![Kết quả](/image/done25.png)