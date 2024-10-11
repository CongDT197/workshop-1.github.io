---
title: "ACM Configuration"
date: "2024-10-08T14:07:07+07:00"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

{{< img src="images/4.acm/acm.png" title="acm logo" >}}

## What is AWS Certificate Manager (ACM)?

**AWS Certificate Manager (ACM)** is a service provided by Amazon Web Services (AWS) that simplifies and automates the management of SSL/TLS certificates. SSL/TLS are critical security protocols that encrypt data transmitted between servers and browsers, protecting sensitive information from being compromised.

## Key Benefits of ACM with SSL

- **Automated certificate management**: ACM automatically creates, issues, and renews SSL/TLS certificates without manual intervention, reducing the risk of expired certificates and lessening the administrative burden.
- **Strong security**: ACM ensures that all connections to your applications and websites are encrypted with SSL/TLS, protecting user data during transmission.
- **Easy integration with AWS services**: ACM seamlessly integrates with other AWS services like **Elastic Load Balancing**, **Amazon CloudFront**, and **Amazon API Gateway**, allowing quick deployment of SSL/TLS certificates without complex configurations.
- **Free public certificates**: ACM provides free public SSL certificates for domains used within AWS, saving costs for businesses.

---

Using **AWS Certificate Manager (ACM)** is an ideal solution for applications and websites requiring strong, automated, and efficient security on the AWS platform.

## ACM Configuration

1. On the List certificates screen, select **Request**.

   {{< img src="images/4.acm/acm-1.png" title="acm 1" >}}

2. In the Fully qualified domain name field, enter `workshop1.kongtran.online`.

   {{< img src="images/4.acm/acm-2.png" title="acm 2" >}}

3. Scroll down and select **Request**.

   {{< img src="images/4.acm/acm-3.png" title="acm 3" >}}

4. You will now have a Certificate with a `pending validation` status. Copy the CNAME name and CNAME value for the domain.

   {{< img src="images/4.acm/acm-4.png" title="acm 4" >}}

5. In your domain management page, add a CNAME with the copied name and value, then click **Add Record**.

   {{< img src="images/4.acm/acm-5.png" title="acm 5" >}}

6. The certificate validation may take a few minutes. Once the validation is successful, you will see the **"Status"** marked as `Issued`, like this:

   {{< img src="images/4.acm/acm-6.png" title="acm 6" >}}

   {{% notice info %}}
   **Note:** If the Certificate validation status is `Failed`, your domain may need a CAA for checking. [AWS CAA troubleshooting guide](https://docs.aws.amazon.com/acm/latest/userguide/troubleshooting-caa.html)
   {{% /notice %}}
