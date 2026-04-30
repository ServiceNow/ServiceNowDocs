---
title: Create a Workday connection
description: Create connection and credential records for the Workday ESG integration so that you can establish a new connection.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Workday, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Create a Workday connection

Create connection and credential records for the Workday ESG integration so that you can establish a new connection.

## Before you begin

Role required: sn\_esg.admin

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social and Governance** &gt; **Workday Integration for ESG Management** &gt; **Connection &amp; Credential Alias**.

2.  On the Connection and Credentials Aliases form, select the **Create New Connection &amp; Credential** related link.

    Contact your Workday administrator to obtain the information for the required fields.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection information|
    |Connection name|Name of the OAuth connection.|
    |Connection URL|Workday Connection URL.|
    |Soap version|Latest version of simple object access protocol \(SOAP\) available in Workday|
    |Tenant name|Tenant Name of Workday.|
    |Credential information|
    |Credential name|Name of the OAuth credential.|
    |OAuth Client ID|OAuth Client ID configured in Workday.|
    |OAuth Client Secret|OAuth Client Secret configured in Workday.|
    |OAuth Redirect URL|OAuth callback endpoint. This field is automatically set.|
    |Auth URL|Workday OAuth Server's auth code flow endpoint.|
    |Token URL|Workday OAuth Server's token endpoint.|

4.  Select **Create and Get OAuth Token**.


## Result

A new connection is created in the connections related list.

## What to do next

Configure the Workday reports. See the [Workday ESG Integration Workday Reports' Configuration \[KB1220842\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1220842) article in the Now Support Knowledge Base article in the Now Support Knowledge Base.

