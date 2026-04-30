---
title: Set up the AWS IAM spoke
description: Integrate the ServiceNow instance and AWS IAM using AWS credential to authenticate ServiceNow requests.Create Credential record for your AWS IAM account. The AWS IAM spoke connection and credential alias uses this credential to perform actions on AWS IAM.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [AWS IAM Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the AWS IAM spoke

Integrate the ServiceNow instance and AWS IAM using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the AWS IAM spoke
-   Role required: admin

## Create Credential record for the AWS IAM spoke

Create Credential record for your AWS IAM account. The AWS IAM spoke connection and credential alias uses this credential to perform actions on AWS IAM.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **AWS IAM**.

3.  From the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **AWS Credentials**.

5.  On the form, fill these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `AWS Credentials`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to IAM.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to IAM.

</td></tr><tr><td>

Credential alias

</td><td>

Associated credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AWS IAM Auth Algo**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


### Result

The credential record the AWS IAM spoke is created.

