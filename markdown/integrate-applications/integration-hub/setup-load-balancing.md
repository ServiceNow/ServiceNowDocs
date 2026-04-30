---
title: Set up the AWS Elastic Load Balancing spoke
description: Integrate the ServiceNow instance and AWS Elastic Load Balancing account using AWS credential to authenticate ServiceNow requests.Create credential record for the AWS Elastic Load Balancing account. The AWS Elastic Load Balancing spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [AWS Elastic Load Balancing Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the AWS Elastic Load Balancing spoke

Integrate the ServiceNow instance and AWS Elastic Load Balancing account using AWS credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the AWS Elastic Load Balancing spoke.
-   Role required: admin.

## Create Credential record for the AWS Elastic Load Balancing spoke

Create credential record for the AWS Elastic Load Balancing account. The AWS Elastic Load Balancing spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **AWS\_Elastic\_Load\_Balancing**.

3.  In the **Credentials** tab, click **New**.

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

Name to uniquely identify the connection record. For example, enter `Elastic Load Balancing Cred`.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Access Key ID

</td><td>

Access Key ID of the user with full access to AWS Elastic Load Balancing.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret Access Key of the user with full access to AWS Elastic Load Balancing.

</td></tr><tr><td>

Credential alias

</td><td>

Associated credential record.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AmazonElasticLoadBalancingAuthAlgo**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>6.  Right-click the form header and click **Submit**.


