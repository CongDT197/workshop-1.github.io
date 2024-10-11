---
title: "Tạo S3 bucket"
date: "2024-10-08T14:07:07+07:00"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

1. Đầu tiên, ta chọn **"Create Bucket"**

{{< img src="images/3.s3/s3-1.png" title="s3-1" >}}

2. Ở giao diện tạo S3, chúng ta nhập tên bucket `kong-static-web`
   Chọn **"ACLs enabled"**
   {{% notice info %}}
   **Chú ý:** tên bucket là duy nhất nên các bạn có thể sử dụng tên bucket khác.
   {{% /notice %}}

{{< img src="images/3.s3/s3-2.png" title="s3-2" >}}

3. Chọn **"Block all public access"** vì chúng ta sử dụng **Cloudfront** nên chỉ muốn người dùng truy cập qua CloudFront để tốc độ nhanh hơn

{{< img src="images/3.s3/s3-3.png" title="s3-2" >}}

4. Scroll tới cuối trang và chọn **"Create Bucket"**

{{< img src="images/3.s3/s3-4.png" title="s3-4" >}}
