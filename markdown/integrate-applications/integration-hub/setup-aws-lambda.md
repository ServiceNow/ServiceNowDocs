---
title: Set up the AWS Lambda spoke
description: Integrate the ServiceNow instance and AWS Lambda account using AWS credential to authenticate ServiceNow requests.Create a credential record for your AWS Lambda account. The AWS Lambda spoke connection and credential alias uses this credential to perform actions on AWS Lambda.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [AWS Lambda Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the AWS Lambda spoke

Integrate the ServiceNow instance and AWS Lambda account using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the [AWS IAM Spoke](../concept/aws-iam-spoke.md)
-   Activate the AWS Lambda spoke
-   Role required: admin

## Create a credential record for the AWS Lambda spoke

Create a credential record for your AWS Lambda account. The AWS Lambda spoke connection and credential alias uses this credential to perform actions on AWS Lambda.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **AWS\_Lambda**.

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

Name to uniquely identify the connection record. For example, enter `Lambda Credentials`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to AWS Lambda.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to AWS Lambda.

</td></tr><tr><td>

Credential alias

</td><td>

Associated credential records of the AWS IAM spoke and AWS Lambda spoke.![AWS Lambda and AWS IAM credential alias records](../image/cred-aws-lambda.png)

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AWS IAM Auth Algo**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


### Result

The credential record the AWS Lambda spoke is created.

