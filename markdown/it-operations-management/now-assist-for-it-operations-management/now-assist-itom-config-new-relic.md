---
title: Configure the New Relic analysis AI agent
description: Connect the New Relic analysis AI agent to your New Relic instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring AI agents for Now Assist for ITOM, Configuring Now Assist for IT Operations Management \(ITOM\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Configure the New Relic analysis AI agent

Connect the New Relic analysis AI agent to your New Relic instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.

## Before you begin

Before configuring the New Relic analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   [Integrate New Relic with Event Management](../../event-management/task/new-relic-events-integration.md).
-   Copy your New Relic API key.

    The New Relic API key must be a user key, also known as a personal API key.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **New Relic analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d576995e142">

Field

</th><th align="left" id="d576995e145">

Description

</th></tr></thead><tbody><tr><td id="d576995e151">

**Connection Name**

</td><td>

Name of your New Relic connection. This name helps you identify it later. For example, New Relic Prod.

</td></tr><tr><td id="d576995e166">

**Connection URL**

</td><td>

URL of the New Relic AI API: `https://nrai-streaming.service.newrelic.com`. The connection URL might vary by region or account.

</td></tr><tr><td id="d576995e181">

**API Key**

</td><td>

New Relic API key.

</td></tr><tr><td id="d576995e192">

**Header Name**

</td><td>

Header name for the New Relic API key: `X-API-Key`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the New Relic analysis AI agent to use it in the Analyze alert impact agentic workflow. In AI Agent Studio, navigate to Create and manage, find the New Relic analysis AI agent, and turn on the agent in the Define key requirements screen.

**Note:** While working in AI Agent Studio, make sure that the Alert information retrieval AI agent is active. It's also required for the Analyze alert impact agentic workflow.

To learn more about using the New Relic analysis AI agent in the Analyze alert impact agentic workflow, see [Use the Analyze alert impact agentic workflow](now-assist-itom-use-aia.md).

**Parent Topic:**[Configuring AI agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

