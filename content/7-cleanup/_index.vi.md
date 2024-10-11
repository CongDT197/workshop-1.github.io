+++
title = "Dọn dẹp tài nguyên"
date = 2024
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

Chúng ta có các bước để xoá resource

### Xoá Cloudfront

1. Vào **Cloudfront** -> Chọn Distribution -> **Disable**
   {{< img src="images/7.clean/clear-1.png" title="03-clean" >}}

2. Đợi 7-10 phút để Cloudfront disabled và có thể xoá
   {{< img src="images/7.clean/clear-3.png" title="03-clean" >}}

3. Xoá cloudfront
   {{< img src="images/7.clean/clear-4.png" title="03-clean" >}}

### Xoá Origin Access

1. Vào **Origin Access** -> Chọn OAI cần xóa -> **Delete**
   {{< img src="images/7.clean/clear-5.png" title="03-clean" >}}

2. Chọn Delete
   {{< img src="images/7.clean/clear-6.png" title="03-clean" >}}

### Xoá Certificates

1. Vào **ACM** -> Chọn certificate cần xóa -> **Delete**
   {{< img src="images/7.clean/clear-7.png" title="03-clean" >}}

2. Chọn Delete
   {{< img src="images/7.clean/clear-8.png" title="03-clean" >}}

### Xoá S3

1. Chúng ta phải xoá tất cả các object bên trong bằng cách chọn tất cả sau đó chọn **"Delete"**

   {{< img src="images/7.clean/clear-9.png" title="03-clean" >}}

2. Gõ `permanently delete` và click **"Delete objects"**

   {{< img src="images/7.clean/clear-9.1.png" title="03-clean" >}}

3. Sau khi bucket đã rỗng, chúng ta quay lại, chọn bucket để xóa
   {{< img src="images/7.clean/clear-9.2.png" title="03-clean" >}}

4. Xác nhận
   {{< img src="images/7.clean/clear-9.3.png" title="03-clean" >}}

{{% notice note %}}
Vậy là chúng ta đã hoàn thành workshop 1, chúc các bạn một ngày vui vẻ.
{{% /notice %}}
