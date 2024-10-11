---
title: "Cấu hình Cloudfront"
date: "2024-10-08T14:07:07+07:00"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

{{< img src="images/4.cloudfront/cloudfront.png" title="cloudfront logo" >}}

### Tổng quan

**Amazon CloudFront** là dịch vụ phân phối nội dung (CDN) của AWS, cho phép truyền tải dữ liệu, video, ứng dụng và API đến người dùng với độ trễ thấp và tốc độ cao. Đối với static web, CloudFront giúp cải thiện hiệu suất bằng cách lưu trữ các nội dung tĩnh như HTML, CSS, JavaScript, và hình ảnh tại các edge location gần với người dùng hơn. Điều này không chỉ giảm thời gian tải trang mà còn giảm tải cho máy chủ gốc, giúp website hoạt động mượt mà và bảo mật hơn nhờ tích hợp SSL/TLS, giảm tấn công DDoS.

Ta có thể sử dụng **Cloudfront** để chuyển hướng HTTP sang HTTPS cho **Static Web Hosting S3**, đồng thời triển khai **WAF** để tăng cường bảo mật.

### Cấu hình Cloudfront

1. Tại màn hình service **"Cloudfront"**, Chọn **"Create a CloudFront distribution"**

{{< img src="images/5.cloudfront/cf-1.png" title="cloudfront-1" >}}

2. Tại mục **Origin domain**, chọn bucket đã tạo ở mục trước

{{< img src="images/5.cloudfront/cf-2.png" title="cloudfront-2" >}}

3. Tại mục **Origin access** chúng ta chọn:
   - Chọn **"Legacy access identities"**
   - Chọn **"Yes, update the bucket policy"**
   - Chọn **"Create new OAI"**
   - Chọn **"Create"**

{{< img src="images/5.cloudfront/cf-3.png" title="cloudfront-3" >}}

4. Tại **Default Cache Behavior** > **"View"** Chọn **"Redirect HTTP to HTTPS"**

{{< img src="images/5.cloudfront/cf-4.1.png" title="cloudfront-4.1" >}}

5. Để mặc định

{{< img src="images/5.cloudfront/cf-5.1.png" title="cloudfront-5.1" >}}

6.

- Mục **"Web Application Firewall"** chúng ta chọn **"Do not enable security protection"**

- Mục **"Settings"** chọn **"Use North America, Europe, Asia, Middle East, and Africa"**
- Mục **"Alternate domain name"** nhập domain name `workshop1.kongtran.online` đã tạo certificate ở bước trước
  {{< img src="images/5.cloudfront/cf-4.png" title="cloudfront-4" >}}

7.

- Mục **Custome SSL certificate**, chọn ACM certificate mà ta đã tạo ở bước trước
- Cuối cùng, kéo tới cuối và chọn **"Create distribution"**
  {{< img src="images/5.cloudfront/cf-5.png" title="cloudfront-5" >}}

8. Việc deploy **CloudFront** sẽ mấy 7-10 phút, sau khi deploy thành công ta sẽ nhận được Last modified như sau

{{< img src="images/5.cloudfront/cf-6.png" title="cloudfront-6" >}}

9. Truy cập trang quản lý domain, thêm CNAME với name là `workshop1`, value là giá trị **Distribution domain name** của Distribution CloudFront đã tạo

{{< img src="images/5.cloudfront/cf-7.png" title="cloudfront-7" >}}
