---
title: "S3 Configuration"
date: "2024-10-08T14:07:07+07:00"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{< img src="images/3.s3/s3.png" title="s3 logo" >}}

## Introduction to AWS S3

**Amazon Simple Storage Service (Amazon S3)** is a cloud-based object storage service provided by AWS, designed for storing and retrieving data with high durability, flexible scalability, and optimized cost. S3 allows users to store any amount of data in the form of objects and manage them within buckets. Data is protected through encryption features, access control, and versioning, meeting security and backup requirements.

S3 supports important features such as:

- **Data encryption** to protect information.
- **Detailed access management** with IAM policies, bucket policies, and Pre-signed URLs.
- **Versioning** to protect data from accidental deletion or overwriting.

**Amazon S3** is designed to ensure availability up to 99.999999999% and stores data for millions of applications used by companies around the world.

## Static Website Hosting with S3

AWS S3 offers **Static Website Hosting**, which allows you to easily store and distribute static websites directly from an S3 bucket. Static websites consist of HTML, CSS, and JavaScript files that do not require server-side processing. This feature is ideal for simple web projects or landing pages.

### Key Features:

- **Store static web files** like HTML, CSS, and JS in an S3 bucket.
- **Distribute content** via the S3 URL or integrate with **Amazon CloudFront** for enhanced speed and security with **SSL**.
- **Low cost**: No need for complex servers, pay only for storage and bandwidth used.

With **S3 Static Website Hosting**, you can quickly, securely, and cost-effectively deploy static websites.

### Content

3.1. [Create S3 bucket](3.1-create-bucket/)\  
3.2. [Enable static web hosting](3.2-config-static-web/)
