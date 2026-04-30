---
title: Set up the Amazon CloudWatch spoke
description: Integrate the ServiceNow instance and Amazon CloudWatch by using the AWS credentials to authenticate ServiceNow requests.Create a credential record for the Amazon CloudWatch Specify whether record is for a host, instance, server, custom application, or account:account. The Amazon CloudWatch Spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Amazon CloudWatch Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon CloudWatch spoke

Integrate the ServiceNow instance and Amazon CloudWatch by using the AWS credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Amazon CloudWatch spoke.
-   Role required: admin

## Create a credential record for the Amazon CloudWatch spoke

Create a credential record for the Amazon CloudWatch account. The Amazon CloudWatch Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **AWS Credentials**.

4.  On the form, fill these values.

<table id="table_e1z_4w4_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, Amazon CloudWatch Cred.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of your AWS account.

 Access Key ID of the user with full access to Amazon CloudWatch.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of your AWS account.

 Secret Access Key of the user with full access to Amazon CloudWatch.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AmazonCloudWatchAlgo**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias associated with the spoke. `AWS_Cloud_Watch`

</td></tr></tbody>
</table>5.  Right-click the form header and click **Submit**.


