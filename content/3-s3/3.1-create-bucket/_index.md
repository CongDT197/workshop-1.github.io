---
title: "Create S3 Bucket"
date: "2024-10-08T14:07:07+07:00"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

1. First, select **"Create Bucket"**

{{< img src="images/3.s3/s3-1.png" title="s3-1" >}}

2. On the S3 creation page, enter the bucket name `kong-static-web`  
   Select **"ACLs enabled"**  
   {{% notice info %}}
   **Note:** The bucket name must be unique, so feel free to use a different name.
   {{% /notice %}}

{{< img src="images/3.s3/s3-2.png" title="s3-2" >}}

3. Choose **"Block all public access"** because we will use **CloudFront** to ensure users access the content faster through the CDN.

{{< img src="images/3.s3/s3-3.png" title="s3-2" >}}

4. Scroll to the bottom of the page and select **"Create Bucket"**

{{< img src="images/3.s3/s3-4.png" title="s3-4" >}}
