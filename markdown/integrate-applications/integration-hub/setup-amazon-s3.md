---
title: Set up the Amazon S3 spoke
description: Use Amazon S3 as file storage in place of attachments in ServiceNow. Adds Amazon S3 storage to your ServiceNow instance and enables users to reference Amazon S3 files in ServiceNow records.Create Credential record for your AWS account. The Create a credential record for the Amazon S3 spoke to enable the spoke to connect to the Amazon S3 host. After connecting, the spoke can perform various actions on Amazon S3.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Amazon S3 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon S3 spoke

Use Amazon S3 as file storage in place of attachments in ServiceNow. Adds Amazon S3 storage to your ServiceNow instance and enables users to reference Amazon S3 files in ServiceNow records.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon S3 spoke
-   Role required: admin

## Create Credential record for the Amazon S3 spoke

Create Credential record for your AWS account. The Create a credential record for the Amazon S3 spoke to enable the spoke to connect to the Amazon S3 host. After connecting, the spoke can perform various actions on Amazon S3.

### Before you begin

Create the AWS access key ID and the secret access key. For more information, see [create secret access key and key ID from AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/iam/create-access-key.html).

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the alias record for **Amazon S3**.

3.  From the **Credentials** tab, click **New**.

4.  Select AWS Credentials.

5.  On the form, fill these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `S3 Credentials`.

</td></tr><tr><td>

Active

</td><td>

Select **Active** to use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of your AWS account.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of your AWS account.

</td></tr><tr><td>

Credential alias

</td><td>

`sn_amazon_s3_spokeAmazon S3`

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Amazon S3**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>    **Note:** To create the Access key ID and secret access key, log into the AWS console. From your account menu, select **My Security Credentials**.

6.  Click **Submit**.


### Result

The credential record for the Amazon S3 spoke is created.

