---
title: Set up the Jamf spoke
description: Integrate the ServiceNow instance and Jamf instance using the Jamf credential to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Jamf Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Jamf spoke

Integrate the ServiceNow instance and Jamf instance using the Jamf credential to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jamf spoke.
-   Role required: admin.

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record, **Jamf**.

3.  Click the **Create New Connection &amp; Credential** related link.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to your Jamf instance in this format: `https://<Instance-name>.jamfcloud.com/`.|
    |Credential Name|Name to identify the credential record.|
    |User Name|User name of the Jamf account.|
    |Password|Password of the Jamf account.|
    |Connection URL|Base URL to connect to your Jamf instance in this format: `https://<Instance-name>.jamfcloud.com/`.|

5.  Click **Create**.

    **Note:** If required, you can get token and revoke token by creating a new credential record for the default connection ad credential alias record.

    ![Get and revoke token.](../image/csd2-jamf-cred2.png)


