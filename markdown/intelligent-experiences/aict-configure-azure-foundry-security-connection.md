---
title: Add an Azure AI Foundry connection
description: Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-azure-foundry-security-connection.html
release: australia
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring security connections, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Add an Azure AI Foundry connection

Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

## Before you begin

Confirm the following:

-   You have an Azure AI Foundry agent already discovered in AI Control Tower inventory.
-   You have an Azure AD app registration \(service principal\) with a role assignment that permits disabling and enabling agent applications on the target resource group.

Role required: sn\_ai\_governance.ai\_steward

## About this task

Adding this connection has two parts: first you create a connection and credential alias that stores your Azure credentials, then you attach that alias to the security connector in AI Control Tower.

## Procedure

1.  Navigate to **Connection &amp; Credential Aliases** \(`sys_alias.list`\).

2.  Select **New**, set **Type** to **Credential**, and select **Submit**.

3.  In the resulting alias record, create a credential and fill in the fields.

4.  Select **Submit**.

    The Connection &amp; Credential Alias record now has this credential attached.

5.  Navigate to **AI Control Tower** &gt; **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

6.  On the **Available connectors** sub-tab, select **Azure AI Foundry**.

7.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Unique, descriptive name for this connection.|
    |**Connection Alias**|The Connection &amp; Credential Alias record you created in the previous steps.|
    |**Active**|Select this option.|

8.  Select **Submit**.


## Result

The connector appears on the **Established connections** sub-tab. AI Control Tower can now use this connection to enforce policies and apply AI agent containment using kill switch protocol to agents running on the connected Azure AI Foundry service.

**Parent Topic:**[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-security-connections.md)

