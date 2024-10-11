---
title: "Kích hoạt static web"
date: "2024-10-08T14:07:07+07:00"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

#### Build source code

1. Đầu tiên chúng ta cần clone [source code mình đã chuẩn bị ở đây](https://github.com/CongDT197/react-sample)
2. Chạy lần lượt các lệnh sau:
   - npm i
   - npm run build
   - Sau khi chạy xong 2 lệnh trên, chúng ta sẽ có thư mục dist có hình dạng như sau:
     {{< img src="images/3.s3/dist.png" title="dist" >}}
3. Ở bucket **"kong-static-web"** đã tạo ở bước trước, ta chọn **"Upload"**
   {{< img src="images/3.s3/s3-5.png" title="s3-5" >}}
4. Chọn **"Add files"** và chọn toàn bộ file trong thư mục dist vừa được build, bấm **"Upload"**
   {{< img src="images/3.s3/s3-6.png" title="s3-6" >}}

#### Bật S3 static

1. Ở bucket **"kong-static-web"** chọn tab **"Properties"**

{{< img src="images/3.s3/s3-7.png" title="s3-7" >}}

3. Kéo xuống dưới, ở mục **Static Website Hosting** chọn **"Edit"**

{{< img src="images/3.s3/08-s3.png" title="08-s3" >}}

4. Static website hosting
   - Chọn **"Enable"**
   - Ở mục **Index document** Chúng ta nhập **"index.html"** (home page sẽ load file **index.html** của chúng ta)
   - Cuối cùng, chọn **"Save Changes"**
     {{< img src="images/3.s3/s3-8.png" title="s3-8" >}}
     {{< img src="images/3.s3/s3-9.png" title="s3-9" >}}
