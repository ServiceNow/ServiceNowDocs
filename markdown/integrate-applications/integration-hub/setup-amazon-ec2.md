---
title: Set up the Amazon EC2 spoke
description: Integrate the ServiceNow instance and Amazon EC2 using AWS credentials to authenticate ServiceNow requests.Create Credential records for the Amazon EC2 instance. The Amazon EC2 spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 1
breadcrumb: [Amazon EC2 Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Amazon EC2 spoke

Integrate the ServiceNow instance and Amazon EC2 using AWS credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon EC2 spoke
-   Role required: admin

## Create Credentials record for the Amazon EC2 spoke

Create Credential records for the Amazon EC2 instance. The Amazon EC2 spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for Amazon\_EC2.

3.  From the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **AWS Credentials**.

5.  On the form, fill these values.

<table id="choicetable_v11_rdx_glb"><thead><tr><th align="left" id="d535908e192">

Field

</th><th align="left" id="d535908e195">

Description

</th></tr></thead><tbody><tr><td id="d535908e201">

**Name**

</td><td>

Name to uniquely identify the connection record. For example, enter `AWS Credentials`.

</td></tr><tr><td id="d535908e213">

**Active**

</td><td>

Option to actively use the credential record.

</td></tr><tr><td id="d535908e222">

**Access Key ID**

</td><td>

Access Key ID of the user with full access to EC2.

</td></tr><tr><td id="d535908e231">

**Secret Access Key**

</td><td>

Secret Access Key of the user with full access to EC2.

</td></tr><tr><td id="d535908e241">

**Credential alias**

</td><td>

Associated credential record.

</td></tr><tr><td id="d535908e250">

**Authentication Algorithm**

</td><td>

Custom authentication algorithm for outbound signing requests. Select **AmazonEC2AuthAlgo**.**Note:** Do not directly modify the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


