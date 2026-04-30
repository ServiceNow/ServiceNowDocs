---
title: Store details of the Jamf server
description: Create a server instance record to discover applications and store details of the Jamf server.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Store details of the Jamf server

Create a server instance record to discover applications and store details of the Jamf server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **JAMF** &gt; **Server instances**.

2.  Click **New**.

3.  On the form, fill there values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the server instance record.|
    |Connection &amp; Credential Alias|Connection and credential alias you had configured while setting up the Jamf spoke. For example, **Jamf**.|

    **Note:** You can use only the default connection and credential alias records that have been shipped along with the [Jamf Spoke](../concept/jamf-spoke.md).

4.  Right-click the form header and click **Submit**.

5.  Click the **Discover Now** related link to discover all applications and retrieve data from the server.

    The Discover and Store Data subflow is triggered. Data is retrieved and in stored in the [Jamf Spoke](../concept/jamf-spoke.md) tables.


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

