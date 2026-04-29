---
title: Create a credential record for the SuccessFactors Learning spoke
description: Create a credential record for the spoke. The SuccessFactors Learning connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SuccessFactors Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a credential record for the SuccessFactors Learning spoke

Create a credential record for the spoke. The SuccessFactors Learning connection and credential alias uses these credentials to authorize actions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`.

3.  Select **SuccessFactors Learning REST Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, `Local Credentials`.|
    |Active|Option to actively use the credential record.|
    |Username|Username to log in to the local ServiceNow instance.|
    |Company ID|Company ID information provided by the client.|
    |User type|Password to log in to the local ServiceNow instance.|
    |Resource type|Resource type information provided by the client.|
    |Client ID|A unique string representing the registration information provided by the client.|
    |Client Secret|A secret code known only to the application and the authorization server.|

5.  Right-click the form header and click **Submit**.


