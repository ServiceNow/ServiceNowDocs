---
title: Configure the Kentik analysis AI agent
description: Connect the Kentik analysis AI agent to your Kentik instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring AI agents for Now Assist for ITOM, Configuring Now Assist for IT Operations Management \(ITOM\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Configure the Kentik analysis AI agent

Connect the Kentik analysis AI agent to your Kentik instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.

## Before you begin

Before configuring the Kentik analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   [Integrate Kentik alerts with Event Management](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2113973).
-   Copy your Kentik connection URL, API token, and the email address associated with the API token.

    The Kentik API token requires this permission: Can view devices.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Kentik analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Connection Name**|Name of your Kentik connection. This name helps you identify it later. For example, Kentik Prod.|
    |**Connection URL**|URL of your Kentik instance. Kentik URLs follow this format: `https://<your-resource-name>.api.kentik.com`.|
    |**User Email**|Email address associated with the Kentik API token.|
    |**API Token**|Kentik API token.|

5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Kentik analysis AI agent to use it in the Analyze alert impact agentic workflow. In AI Agent Studio, navigate to Create and manage, find the Kentik analysis AI agent, and turn on the agent in theDefine key requirements screen.

**Note:** While working in AI Agent Studio, make sure that the Alert information retrieval AI agent is active. It's also required for the Analyze alert impact agentic workflow.

To learn more about using the Kentik analysis AI agent in the Analyze alert impact agentic workflow, see [Use the Analyze alert impact agentic workflow](now-assist-itom-use-aia.md).

**Parent Topic:**[Configuring AI agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

