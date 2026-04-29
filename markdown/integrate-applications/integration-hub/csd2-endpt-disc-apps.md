---
title: Store details of the provider server
description: Create a server instance record to discover applications and store details of the provider server.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Endpoint Configuration Manager, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Store details of the provider server

Create a server instance record to discover applications and store details of the provider server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Microsoft Endpoint Configuration Manager** &gt; **Server instances**.

2.  Click **New**.

3.  On the form, fill there values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the server instance record.|
    |Powershell Connection &amp; Credential Alias|Powershell connection and credential alias you had configured while setting up the Microsoft Endpoint Configuration Manager spoke. For example, **Microsoft Endpoint Configuration Spoke**.|
    |JDBC Connection &amp; Credential Alias|JDBC connection and credential alias you had configured while setting up the Microsoft Endpoint Configuration Manager spoke. For example, **Microsoft Endpoint Configuration JDBC**.|

    **Note:** You can use only the default connection and credential alias records that have been shipped along with the [Microsoft Endpoint Configuration Manager Spoke](../concept/ms-endpoint.md).

4.  Right-click the form header and click **Submit**.

5.  Click the **Discover Now** related link to discover all applications and retrieve data from the server.

    The Discover and Store Data subflow is triggered. Data is retrieved and in stored in the [Microsoft Endpoint Configuration Manager Spoke](../concept/ms-endpoint.md) tables.


**Parent Topic:**[CSD 2.0 for Microsoft Endpoint Configuration Manager](../concept/csd2.md)

