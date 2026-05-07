---
title: Configure the New Relic analysis AI agent
description: Configure the New Relic analysis AI agent for the analyze alert impact agentic workflow. After you configure the agent, the workflow can surface information from New Relic to help you investigate alerts.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring agents for Now Assist for ITOM, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the New Relic analysis AI agent

Configure the New Relic analysis AI agent for the analyze alert impact agentic workflow. After you configure the agent, the workflow can surface information from New Relic to help you investigate alerts.

## Before you begin

Before configuring the New Relic analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   [Integrate New Relic with Event Management](../../event-management/task/new-relic-events-integration.md).
-   Copy your New Relic API key.

    The New Relic API key must be a user key, also known as a personal API key.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **New Relic analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d344220e154">

Field

</th><th align="left" id="d344220e157">

Description

</th></tr></thead><tbody><tr><td id="d344220e163">

**Connection Name**

</td><td>

Name of your New Relic connection. This name helps you identify it later. For example, New Relic Prod.

</td></tr><tr><td id="d344220e178">

**Connection URL**

</td><td>

URL of the New Relic AI API: `https://nrai-streaming.service.newrelic.com`. The connection URL might vary by region or account.

</td></tr><tr><td id="d344220e193">

**API Key**

</td><td>

New Relic API key.

</td></tr><tr><td id="d344220e204">

**Header Name**

</td><td>

Header name for the New Relic API key: `X-API-Key`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the New Relic analysis AI agent to use it in the analyze alert impact agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the New Relic analysis AI agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the New Relic analysis AI agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about using the New Relic analysis AI agent in the analyze alert impact agentic workflow, see [Use the analyze alert impact agentic workflow](now-assist-itom-use-aia.md).

**Parent Topic:**[Configuring agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

