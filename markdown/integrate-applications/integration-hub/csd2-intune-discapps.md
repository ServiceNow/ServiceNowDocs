---
title: Store details of the Microsoft Intune server
description: Create a server instance record to discover applications and store details of the Microsoft Intune server.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Intune, Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Store details of the Microsoft Intune server

Create a server instance record to discover applications and store details of the Microsoft Intune server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Microsoft Intune** &gt; **Server instances**.

2.  Click **New**.

3.  On the form, fill there values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the server instance record.|
    |Connection &amp; Credential Alias|Connection and credential alias you had configured while setting up the Microsoft Intune spoke. For example, **Microsoft\_Intune**.|

    **Note:** You can use only the default connection and credential alias records that have been shipped along with the [Microsoft Intune Spoke](../concept/ms-intune-spoke.md).

4.  Right-click the form header and click **Submit**.

5.  Click the **Discover Now** related link to discover all applications and retrieve data from the server.

    The Discover and Store Data subflow is triggered. Data is retrieved and in stored in the [Microsoft Intune Spoke](../concept/ms-intune-spoke.md) tables.


**Parent Topic:**[CSD 2.0 for Microsoft Intune](../concept/csd2-ms-intune.md)

