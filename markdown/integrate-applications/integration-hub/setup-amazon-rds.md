---
title: Set up the Amazon RDS spoke
description: Integrate the ServiceNow instance and Amazon RDS using AWS credentials to authenticate ServiceNow requests.Create Credential records for the Amazon RDS instance. The Amazon RDS spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 1
breadcrumb: [Amazon RDS Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Amazon RDS spoke

Integrate the ServiceNow instance and Amazon RDS using AWS credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Amazon RDS spoke
-   Role required: admin

## Create Credentials records for the Amazon RDS spoke

Create Credential records for the Amazon RDS instance. The Amazon RDS spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

2.  Open for the record for Amazon RDS.

3.  From the **Credentials** tab, click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

4.  Select **AWS Credentials**.

5.  On the form, fill these fields.

<table id="choicetable_prq_ckx_glb"><thead><tr><th align="left" id="d260936e193">

Field

</th><th align="left" id="d260936e196">

Description

</th></tr></thead><tbody><tr><td id="d260936e202">

**Name**

</td><td>

Name to uniquely identify the connection record. For example, enter `AWS Credentials`.

</td></tr><tr><td id="d260936e214">

**Active**

</td><td>

Option to actively use the credential record.

</td></tr><tr><td id="d260936e223">

**Access Key ID**

</td><td>

Access Key ID of the user with full access to Amazon RDS.

</td></tr><tr><td id="d260936e232">

**Secret Access Key**

</td><td>

Secret Access Key of the user with full access to Amazon RDS.

</td></tr><tr><td id="d260936e242">

**Credential alias**

</td><td>

Associated credential record.

</td></tr><tr><td id="d260936e251">

**Authentication Algorithm**

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Amazon RDS Auth Algorithm**.**Note:** Do not directly modify the default authentication algorithm.

</td></tr></tbody>
</table>6.  Click **Submit**.


