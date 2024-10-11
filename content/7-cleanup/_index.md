+++
title = "Cleanup Resources"
date = 2024
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

We have steps to delete resources.

### Delete CloudFront

1. Go to **CloudFront** -> Select Distribution -> **Disable**
   {{< img src="images/7.clean/clear-1.png" title="03-clean" >}}

2. Wait for 7-10 minutes for CloudFront to disable before you can delete it.
   {{< img src="images/7.clean/clear-3.png" title="03-clean" >}}

3. Delete CloudFront
   {{< img src="images/7.clean/clear-4.png" title="03-clean" >}}

### Delete Origin Access

1. Go to **Origin Access** -> Select the OAI you want to delete -> **Delete**
   {{< img src="images/7.clean/clear-5.png" title="03-clean" >}}

2. Select Delete
   {{< img src="images/7.clean/clear-6.png" title="03-clean" >}}

### Delete Certificates

1. Go to **ACM** -> Select the certificate you want to delete -> **Delete**
   {{< img src="images/7.clean/clear-7.png" title="03-clean" >}}

2. Select Delete
   {{< img src="images/7.clean/clear-8.png" title="03-clean" >}}

### Delete S3

1. You need to delete all objects inside by selecting all and then clicking **"Delete"**.
   {{< img src="images/7.clean/clear-9.png" title="03-clean" >}}

2. Type `permanently delete` and click **"Delete objects"**.
   {{< img src="images/7.clean/clear-9.1.png" title="03-clean" >}}

3. After the bucket is empty, go back and select the bucket to delete.
   {{< img src="images/7.clean/clear-9.2.png" title="03-clean" >}}

4. Confirm deletion.
   {{< img src="images/7.clean/clear-9.3.png" title="03-clean" >}}

{{% notice note %}}
Thus, we have completed workshop 1. Have a nice day!
{{% /notice %}}
