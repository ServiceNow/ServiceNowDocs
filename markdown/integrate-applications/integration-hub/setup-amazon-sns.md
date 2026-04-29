---
title: Set up the Amazon SNS spoke
description: Integrate the ServiceNow instance and Amazon SNS using AWS credential to authenticate ServiceNow requests.Create Credential record for your AWS account. The Amazon SNS spoke uses this credential to perform actions on Amazon SNS.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon SNS Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon SNS spoke

Integrate the ServiceNow instance and Amazon SNS using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon SNS spoke
-   Role required: admin

## About this task

To receive events at your ServiceNow instance from Amazon SNS, see [Receive events at your ServiceNow instance from Amazon SNS](notification-sns.md#). Spoke set up described here enables you to use spoke subflow and actions.

## Create Credential record for the Amazon SNS spoke

Create Credential record for your AWS account. The Amazon SNS spoke uses this credential to perform actions on Amazon SNS.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Amazon SNS**.

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

Name to uniquely identify the connection record. For example, enter `SNS Credentials`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

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

Associated credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **SNS Algorithm**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


### Result

The credential record for the Amazon SNS spoke is created.

