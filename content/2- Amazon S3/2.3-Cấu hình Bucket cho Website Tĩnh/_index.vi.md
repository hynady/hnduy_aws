---
title : "Cấu hình Bucket cho Website Tĩnh"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 2.3 </b> "
---

- Bật tính năng website tĩnh:
  - Trong bucket, chuyển đến "Properties".
  - Cuộn xuống "Static website hosting" và nhấn "Edit".
![Bật tính năng website tĩnh](/image/done7.png)
![Static website hosting](/image/done8.png)


- Chọn "Enable" và nhập tên tệp trang chủ (ví dụ: index.html).
![Nhấn "Enable"](/image/done9.png)
- Nhấn "Save".
![Save](/image/done10.png)

- Cấu hình Quyền Truy Cập Công Khai:
  - Trong phần "Permissions", bạn sẽ thấy một phần tên là "Block public access (bucket settings)".
  - Nhấn "Edit" và chắc chắn rằng các tùy chọn chặn truy cập công khai (Block all public access) đã bị tắt (nghĩa là bucket của bạn sẽ cho phép truy cập công khai).
![Cấu hình Quyền Truy Cập Công Khai](/image/done11.png)

- Sau khi tắt tính năng chặn truy cập công khai, nhấn "Save changes".
![Nhấn "Save changes"](/image/done12.png)

- Vẫn ở trong tab "Permissions", kéo xuống phần Bucket Policy.
- Nếu chưa có chính sách, bạn cần thêm một chính sách để cho phép truy cập công khai tới các tệp trong bucket.
- Nhấn "Edit" trong phần Bucket Policy và thêm đoạn mã sau. Đảm bảo thay thế "my-static-website-lab" bằng tên bucket thực tế của bạn.
![Edit](/image/done13.png)
![Thêm đoạn mã Nhấn "Save changes"](/image/done14.png)
