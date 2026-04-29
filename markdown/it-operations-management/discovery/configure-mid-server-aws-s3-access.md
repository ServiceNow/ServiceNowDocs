---
title: Configure MID Server for AWS S3 access
description: Configure MID Server properties to enable Simple Storage Service \(S3\) access from the ServiceNow AI Platform when performing Systems Manager \(SSM\) Agent discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [AWS SSM discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure MID Server for AWS S3 access

Configure MID Server properties to enable Simple Storage Service \(S3\) access from the ServiceNow AI Platform® when performing Systems Manager \(SSM\) Agent discovery.

## Before you begin

Confirm the following:

-   You have at least one MID Server installed and in the **Up** state. For more information, see [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md).
-   You have an AWS credential that allows the MID Server to access and make API calls into the AWS environment. For more information, see [AWS Access for MID Server](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#midawsaccess).
-   You created a custom S3 bucket with necessary access enabled for the IAM roles. For more information, see [Setting up an S3 Bucket](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#s3bucket) and [Setting up a Policy for accessing the S3 Bucket](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#bucketpolicysetup).

Role required: discovery\_admin

## About this task

Because the SSM Run Command console has a 24,000-character limit, results that exceed this limit must be stored in and retrieved from an S3 bucket. For Put File commands, the S3 bucket also serves as a transfer point between the MID Server and the AWS environment, enabling file delivery to target devices via SSM. To configure the MID Server to support these S3-based operations, set the **mid.discovery.aws\_ssm.s3\_bucket\_name** property to the name of the S3 bucket used for SSM Agent discovery. Then, specify the bucket’s region in the **mid.discovery.aws\_ssm.s3\_bucket\_region** property.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** field, enter `mid.discovery.aws_ssm.s3_bucket_name`.

3.  Double-click the **Value** field to perform inline editing.

4.  Enter the name of the S3 bucket.

5.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.

6.  In the **Name** field, enter `mid.discovery.aws_ssm.s3_bucket_region`.

7.  Double-click the **Value** field to perform inline editing.

8.  Enter the name of the region where the S3 bucket is located.

9.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.


