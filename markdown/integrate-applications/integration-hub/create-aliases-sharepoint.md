---
title: Create aliases for multiple tenants
description: Create a connection and credential alias record for each additional tenant site that you want to support. Select the correct alias in the Tenant record to authorize changes in Microsoft SharePoint Online.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create aliases for multiple tenants

Create a connection and credential alias record for each additional tenant site that you want to support. Select the correct alias in the Tenant record to authorize changes in Microsoft SharePoint Online.

## Before you begin

Role required: admin.

## About this task

If configuring an integration for a single tenant, use the existing **MicrosoftSharepointOnline** alias record.

**Note:**

-   You can use multiple tenants with the **Microsoft SharePoint Graph** connection alias only.
-   Three alias records are available by default with the spoke; Sharepoint Online, SharePoint Graph, and SharePoint Graph Root Site Subscription. Each alias record requires a tenant to be associated with it. If you intend to use all SharePoint Online, Graph, and Root Subscription actions in the spoke, you must ensure that you have created three tenant records in the Tenants tables of the Microsoft SharePoint Online spoke so that each tenant record is associated with its respective alias record.

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click **New**.

    A blank Connection &amp; Credential Alias record opens

3.  On the **Connection &amp; Credential Aliases** form, fill the following values.

    |Field|Value|
    |-----|-----|
    |Name|Unique name|
    |Type|Connection and Credential|
    |Connection type|HTTP|

4.  Click **Submit**.


## What to do next

Associate a credential record and a connection record with the alias to authorize actions on the SharePoint tenant site. Create an alias record and associated connection and credential records for each tenant you want to support.

