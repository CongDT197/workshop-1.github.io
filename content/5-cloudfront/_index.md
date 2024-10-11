---
title: "CloudFront Configuration"
date: "2024-10-08T14:07:07+07:00"
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

{{< img src="images/4.cloudfront/cloudfront.png" title="cloudfront logo" >}}

### Overview

**Amazon CloudFront** is AWS's content delivery network (CDN) service, enabling the distribution of data, videos, applications, and APIs to users with low latency and high transfer speeds. For static websites, CloudFront improves performance by caching static content such as HTML, CSS, JavaScript, and images at edge locations closer to users. This not only reduces page load time but also offloads traffic from the origin server, ensuring smoother website performance and enhanced security via SSL/TLS integration and DDoS protection.

We can use **CloudFront** to redirect HTTP to HTTPS for **S3 Static Web Hosting**, and also implement **WAF** to enhance security.

### CloudFront Configuration

1. On the **"CloudFront"** service screen, select **"Create a CloudFront distribution"**.

   {{< img src="images/5.cloudfront/cf-1.png" title="cloudfront-1" >}}

2. In the **Origin domain** field, select the bucket created in the previous step.

   {{< img src="images/5.cloudfront/cf-2.png" title="cloudfront-2" >}}

3. In the **Origin access** section, select:

   - **"Legacy access identities"**.
   - **"Yes, update the bucket policy"**.
   - **"Create new OAI"**.
   - **"Create"**.

   {{< img src="images/5.cloudfront/cf-3.png" title="cloudfront-3" >}}

4. In **Default Cache Behavior** > **"View"**, select **"Redirect HTTP to HTTPS"**.

   {{< img src="images/5.cloudfront/cf-4.1.png" title="cloudfront-4.1" >}}

5. Leave the other settings at their default values.

   {{< img src="images/5.cloudfront/cf-5.1.png" title="cloudfront-5.1" >}}

6.

- In the **"Web Application Firewall"** section, select **"Do not enable security protection"**.
- In the **"Settings"** section, select **"Use North America, Europe, Asia, Middle East, and Africa"**.
- In the **"Alternate domain name"** field, enter the domain name `workshop1.kongtran.online` that was assigned a certificate in the previous step.

  {{< img src="images/5.cloudfront/cf-4.png" title="cloudfront-4" >}}

7.

- In the **Custom SSL certificate** section, select the ACM certificate created earlier.
- Finally, scroll to the bottom and click **"Create distribution"**.

  {{< img src="images/5.cloudfront/cf-5.png" title="cloudfront-5" >}}

8. The **CloudFront** deployment will take 7-10 minutes. Once successfully deployed, you'll see a **Last modified** status like this:

   {{< img src="images/5.cloudfront/cf-6.png" title="cloudfront-6" >}}

9. Go to your domain management page, and add a **CNAME** with the name `workshop1` and the value as the **Distribution domain name** of the CloudFront distribution you just created.

   {{< img src="images/5.cloudfront/cf-7.png" title="cloudfront-7" >}}
