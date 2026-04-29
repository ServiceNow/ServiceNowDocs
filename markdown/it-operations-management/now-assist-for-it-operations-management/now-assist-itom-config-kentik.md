---
title: Configure the Kentik analysis AI agent
description: Configure the Kentik analysis AI agent for the analyze alert impact agentic workflow. After you configure the agent, the workflow can surface information from Kentik to help you investigate alerts.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring agents for Now Assist for ITOM, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Kentik analysis AI agent

Configure the Kentik analysis AI agent for the analyze alert impact agentic workflow. After you configure the agent, the workflow can surface information from Kentik to help you investigate alerts.

## Before you begin

Before configuring the Kentik analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
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

Activate the Kentik analysis AI agent to use it in the analyze alert impact agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Kentik analysis AI agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the Kentik analysis AI agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about using the Kentik analysis AI agent in the analyze alert impact agentic workflow, see [Use the analyze alert impact agentic workflow](now-assist-itom-use-aia.md).

**Parent Topic:**[Configuring agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

