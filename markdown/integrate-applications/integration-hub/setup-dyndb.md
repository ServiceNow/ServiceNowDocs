---
title: Set up the Amazon DynamoDB spoke
description: Integrate the ServiceNow instance and Amazon DynamoDB account using AWS credential to authenticate ServiceNow requests.Create two Credential records for your Amazon DynamoDB account. The Amazon DynamoDB spoke connection and credential alias uses these credential records to perform actions in your Amazon DynamoDB account.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Amazon DynamoDB Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Amazon DynamoDB spoke

Integrate the ServiceNow instance and Amazon DynamoDB account using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon DynamoDB spoke
-   Role required: admin

## Create Credential records for the Amazon DynamoDB spoke

Create two Credential records for your Amazon DynamoDB account. The Amazon DynamoDB spoke connection and credential alias uses these credential records to perform actions in your Amazon DynamoDB account.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Amazon DynamoDB**.

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

Name to uniquely identify the connection record. For example, enter `Amazon DynamoDB Cred`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to Amazon DynamoDB.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to Amazon DynamoDB.

</td></tr><tr><td>

Credential alias

</td><td>

Associated Amazon DynamoDB credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Amazon DynamoDB**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.

7.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

8.  Open for the record for **Amazon DynamoDB Streams**.

9.  From the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

10. Select **AWS Credentials**.

11. On the form, fill these values.

<table id="table_f1b_mkr_ylb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `Amazon DynamoDB Streams Cred`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to Amazon DynamoDB.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to Amazon DynamoDB.

</td></tr><tr><td>

Credential alias

</td><td>

Associated Amazon DynamoDB Streams credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Amazon DynamoDB Streams**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>12. Click **Submit**.


