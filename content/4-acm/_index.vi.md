---
title: "Cấu hình ACM"
date: "2024-10-08T14:07:07+07:00"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

{{< img src="images/4.acm/acm.png" title="acm logo" >}}

## AWS Certificate Manager (ACM) là gì?

**AWS Certificate Manager (ACM)** là một dịch vụ do Amazon Web Services (AWS) cung cấp, giúp quản lý chứng chỉ số SSL/TLS dễ dàng và tự động hơn. SSL/TLS là các giao thức bảo mật quan trọng giúp mã hóa dữ liệu truyền tải giữa các máy chủ và trình duyệt, bảo vệ thông tin nhạy cảm khỏi bị xâm phạm.

## Lợi ích chính của ACM với SSL

- **Tự động hóa quy trình quản lý chứng chỉ**: ACM tự động tạo, cấp, và gia hạn chứng chỉ SSL/TLS mà không cần quản lý thủ công, giúp giảm thiểu rủi ro hết hạn chứng chỉ và giảm bớt gánh nặng công việc cho quản trị viên.
- **Bảo mật mạnh mẽ**: ACM đảm bảo rằng mọi kết nối đến các ứng dụng và trang web đều được mã hóa bằng SSL/TLS, giúp bảo vệ dữ liệu người dùng trong suốt quá trình truyền tải.

- **Dễ dàng tích hợp với các dịch vụ AWS**: ACM tích hợp liền mạch với các dịch vụ AWS khác như **Elastic Load Balancing**, **Amazon CloudFront**, và **Amazon API Gateway**, cho phép triển khai chứng chỉ SSL/TLS nhanh chóng mà không cần cấu hình phức tạp.

- **Miễn phí chứng chỉ công khai**: ACM cung cấp chứng chỉ SSL công khai miễn phí cho các tên miền sử dụng trong AWS, giúp tiết kiệm chi phí cho các doanh nghiệp.

---

Sử dụng **AWS Certificate Manager (ACM)** là giải pháp lý tưởng cho các ứng dụng và trang web cần bảo mật mạnh mẽ, tự động và hiệu quả trên nền tảng AWS.

## Cấu hình ACM

1. Ở màn hình List certificates, ta chọn **Request**

{{< img src="images/4.acm/acm-1.png" title="acm 1" >}}

2. Ở mục Fully qualified domain name, ta điền vào `workshop1.kongtran.online`

{{< img src="images/4.acm/acm-2.png" title="acm 2" >}}

3. Kéo xuống cuối cùng chọn Request
   {{< img src="images/4.acm/acm-3.png" title="acm 3" >}}

4. Ta sẽ tạo được 1 Certificate có trang thái `pending validation`.
   Copy CNAME name và CNAME value ở domain

   {{< img src="images/4.acm/acm-4.png" title="acm 4" >}}

5. Ở trang quản lý domain, ta thêm CNAME với name và value đã copy ở trên, bấm Add Record
   {{< img src="images/4.acm/acm-5.png" title="acm 5" >}}
6. Việc validation certificate sẽ mất 1 vài phút, khi validate thành công, ta sẽ thu được kết quả **"Status"** `Issued` như sau:

   {{< img src="images/4.acm/acm-6.png" title="acm 6" >}}

   {{% notice info %}}
   **Chú ý:** Nếu Certificate validate có trạng thái `Failed` thì khả lăng domain của bạn cần có CAA cho việc checking. [Hướng dẫn thêm CAA của AWS](https://docs.aws.amazon.com/acm/latest/userguide/troubleshooting-caa.html)
   {{% /notice %}}
