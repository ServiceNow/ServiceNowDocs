---
title: Configure MID Server for AWS KMS access
description: Configure MID Server properties to enable Key Management Service \(KMS\) key access from the ServiceNow AI Platform when performing Systems Manager \(SSM\) Agent discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [AWS SSM discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure MID Server for AWS KMS access

Configure MID Server properties to enable Key Management Service \(KMS\) key access from the ServiceNow AI Platform® when performing Systems Manager \(SSM\) Agent discovery.

## Before you begin

Confirm the following:

-   You have at least one MID Server installed and in the **Up** state. For more information, see [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md).
-   You have an AWS credential that allows the MID Server to access and make API calls into the AWS environment. For more information, see [AWS Access for MID Server](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#midawsaccess).
-   You created a custom AWS KMS key to encrypt sensitive credentials. For more information, see [Create a Customer Managed AWS KMS Key](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#awskey).

Role required: discovery\_admin

## About this task

Using a dedicated key enhances security by verifying that applicative credentials are encrypted and securely retrieved at runtime, without being exposed in plain text. This step is optional and only necessary if you plan to use applicative credentials during discovery. To configure the MID Server to support secure credential handling during SSM Agent discovery, set the **mid.discovery.aws\_ssm.kms\_key\_name** property to the name of the AWS KMS key. Then, set the **mid.discovery.aws\_ssm.kms\_key\_region** property to the region where the key is located.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** field, enter `mid.discovery.aws_ssm.kms_key_name`.

3.  Double-click the **Value** field to perform inline editing.

4.  Enter the name of the KMS key.

5.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.

6.  In the **Name** field, enter `mid.discovery.aws_ssm.kms_key_region`.

7.  Double-click the **Value** field to perform inline editing.

8.  Enter the name of the region where the KMS key is located.

9.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.


