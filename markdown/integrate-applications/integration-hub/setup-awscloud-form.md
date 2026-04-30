---
title: Set up the AWS CloudFormation spoke
description: Integrate the ServiceNow instance and AWS CloudFormation using AWS credential to authenticate ServiceNow requests.Create Credential record for your AWS CloudFormation account. The AWS CloudFormation spoke connection and credential alias uses this credential to perform actions in AWS CloudFormation.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AWS CloudFormation Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the AWS CloudFormation spoke

Integrate the ServiceNow instance and AWS CloudFormation using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the AWS CloudFormation spoke.
-   Role required: admin.

## Create Credential record for the AWS CloudFormation spoke

Create Credential record for your AWS CloudFormation account. The AWS CloudFormation spoke connection and credential alias uses this credential to perform actions in AWS CloudFormation.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Amazon VPC**.

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

Name to uniquely identify the connection record. For example, enter `CloudFormation Credentials`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to AWS CloudFormation.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to AWS CloudFormation.

</td></tr><tr><td>

Credential alias

</td><td>

Associated credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AWS\_CloudFormation**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


### Result

The credential record the AWS CloudFormation spoke is created.

