---
title: Set up the Credly spoke
description: Integrate the ServiceNow instance and Credly by creating a custom OAuth application in Credly to authenticate ServiceNow requests.Create a connection record for your Credly spoke. The Credly connection and credential aliases use these connections to perform actions in Credly.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 1
breadcrumb: [Credly spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Credly spoke

Integrate the ServiceNow instance and Credly by creating a custom OAuth application in Credly to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Credly spoke.
-   Role required: admin

## Create a connection record for Credly spoke

Create a connection record for your Credly spoke. The Credly connection and credential aliases use these connections to perform actions in Credly.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for **Credly**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `<Credly spoke> Connection`.|
    |Credential|Credential record created for Credly. For example, `<Credly spoke> Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |URL builder|Option to use the URL builder to build the connection string.|
    |Connection URL|Base URL to connect to **Credly**. Enter: ``|
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Servers for this connection. If the check box is selected, define the fields in the Advanced MID Server Configuration related list.|
    |Attributes|
    |Organization ID|The ID of the employee's organization in Credly.|

5.  Select **Submit**.


