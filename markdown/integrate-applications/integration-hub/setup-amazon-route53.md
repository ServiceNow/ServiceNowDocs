---
title: Set up the Amazon Route 53 spoke
description: Integrate the ServiceNow instance and Amazon Route 53 by using the AWS credentials to authenticate ServiceNow requests.Create a credential record for the Amazon Route 53 custom application. The Amazon Route 53 spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Amazon Route 53 Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Amazon Route 53 spoke

Integrate the ServiceNow instance and Amazon Route 53 by using the AWS credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Amazon Route 53 spoke
-   Role required: admin

## Create a credential record for the Amazon Route 53 spoke

Create a credential record for the Amazon Route 53 custom application. The Amazon Route 53 spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **AWS Credentials**.

4.  On the form, fill these values.

<table id="table_osq_sqr_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, Amazon Route 53 Cred.

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

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Amazon Route53**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias associated with the spoke. **sn\_amzn\_rout53\_spk.AmazonRoute53**

</td></tr></tbody>
</table>5.  Right-click the form header and click **Submit**.


