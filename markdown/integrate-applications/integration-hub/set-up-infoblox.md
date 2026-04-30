---
title: Set up the Infoblox spoke
description: Integrate the ServiceNow instance and Infoblox using basic authentication to authenticate ServiceNow requests.Create Connection records to your Infoblox account. The Infoblox spoke connection and credential aliases use these connections to perform actions in Infoblox.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Infoblox Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Infoblox spoke

Integrate the ServiceNow instance and Infoblox using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Infoblox spoke.
-   Role required: admin.

## Create a Connection and Credential Alias for Infoblox spoke

Create Connection records to your Infoblox account. The Infoblox spoke connection and credential aliases use these connections to perform actions in Infoblox.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the Infoblox record.

3.  From the **Related Links** section, click **Create New Connection &amp; Credential**.

4.  On the form, fill in these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Unique name to identify the connection. For example, Infoblox Spoke Connection.|
    |Connection URL|Host URL to connect to your Infoblox account.|
    |API Version|API version of Inblox. This field is auto-populated to `v2.11`|
    |User Name|User name of your Infoblox account.|
    |Password|Password of your Infoblox account.|

    ![Create Connection and Credential form for Infoblox spoke](../image/conn-cred-alias-infoblox.png)

5.  Click **Create**.


