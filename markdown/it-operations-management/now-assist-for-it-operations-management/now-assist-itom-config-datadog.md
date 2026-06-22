---
title: Configure the Datadog analysis AI agent
description: Configure the Datadog analysis AI agent to use the Datadog observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-datadog.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure the manage alerts autonomously agentic workflow, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Datadog analysis AI agent

Configure the Datadog analysis AI agent to use the Datadog observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.

## Before you begin

Before configuring the Datadog analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).
-   [Integrate Datadog platform events with Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-events-webhook.md).
-   Copy your Datadog API key and application key.

Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Datadog analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d193546e149">

Field

</th><th align="left" id="d193546e152">

Description

</th></tr></thead><tbody><tr><td id="d193546e158">

**Connection Name**

</td><td>

Name of your Datadog connection. This name helps you identify it later. For example, `Datadog analysis AI agent connection`.

</td></tr><tr><td id="d193546e175">

**Connection URL**

</td><td>

URL of your Datadog instance. Datadog URLs follow this format: `https://api.datadoghq.com`.

</td></tr><tr><td id="d193546e193">

**Datadog API key**

</td><td>

Your Datadog API key.

</td></tr><tr><td id="d193546e207">

**Datadog Application key**

</td><td>

Your Datadog application key.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Datadog analysis AI agent to use it in the manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Datadog analysis AI agent, and turn on the agent in the Select channels and status screen.

To learn more about using the Datadog analysis AI agent in the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.md)

