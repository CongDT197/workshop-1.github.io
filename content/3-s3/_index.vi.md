---
title: "Cấu hình S3"
date: "2024-10-08T14:07:07+07:00"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{< img src="images/3.s3/s3.png" title="s3 logo" >}}

## Giới thiệu về AWS S3

**Amazon Simple Storage Service (Amazon S3)** là một dịch vụ lưu trữ đối tượng trên đám mây do AWS cung cấp, giúp lưu trữ và truy xuất dữ liệu với độ bền cao, khả năng mở rộng linh hoạt, và chi phí tối ưu. S3 cho phép người dùng lưu trữ bất kỳ lượng dữ liệu nào dưới dạng các đối tượng và quản lý chúng trong các bucket. Dữ liệu được bảo vệ với các tính năng mã hóa, kiểm soát truy cập, và quản lý phiên bản, đáp ứng các yêu cầu bảo mật và sao lưu dữ liệu.

S3 hỗ trợ nhiều tính năng quan trọng như:

- **Mã hóa dữ liệu** để bảo vệ thông tin.
- **Quản lý truy cập chi tiết** với IAM policies, bucket policies và Pre-signed URLs.
- **Quản lý phiên bản (Versioning)** giúp bảo vệ dữ liệu khỏi các lỗi xóa hoặc ghi đè không mong muốn.

**Amazon S3** được thiết kế để đảm bảo tính sẵn sàng lên tới 99,999999999% và lưu trữ dữ liệu của hàng triệu ứng dụng cho các công ty trên toàn thế giới.

## Static Website Hosting với S3

AWS S3 cung cấp khả năng **Static Website Hosting**, giúp bạn dễ dàng lưu trữ và phân phối các trang web tĩnh trực tiếp từ S3 bucket. Website tĩnh bao gồm các tệp HTML, CSS và JavaScript không cần xử lý từ phía server. Tính năng này lý tưởng cho các dự án web đơn giản hoặc các trang giới thiệu.

### Các tính năng chính:

- **Lưu trữ tệp web tĩnh** như HTML, CSS, JS trong S3 bucket.
- **Phân phối nội dung** thông qua URL của S3 hoặc tích hợp với **Amazon CloudFront** để tăng tốc độ và bảo mật với **SSL**.
- **Chi phí thấp**: Không yêu cầu máy chủ phức tạp, chỉ trả phí cho dung lượng lưu trữ và băng thông sử dụng.

Với **S3 Static Website Hosting**, bạn có thể dễ dàng triển khai các trang web tĩnh, nhanh chóng, an toàn và tiết kiệm chi phí.

### Content

3.1. [Tạo S3 bucket](3.1-create-bucket/)\
3.2. [Kích hoạt static web](3.2-config-static-web/)
