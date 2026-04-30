---
title: Configure the Datadog analysis AI agent
description: Configure the Datadog analysis AI agent to use the Datadog observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.
locale: en-US
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [Configuring agents and skills for Now Assist for ITOM, Configuring Now Assist for ITOM, Now Assist for ITOM, IT Operations Management]
---

# Configure the Datadog analysis AI agent

Configure the Datadog analysis AI agent to use the Datadog observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.

## Before you begin

Before configuring the Datadog analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   [Integrate Datadog platform events with Event Management](../../event-management/task/datadog-events-webhook.md).
-   Copy your Datadog API key and application key.

Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Datadog analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d317654e142">

Field

</th><th align="left" id="d317654e145">

Description

</th></tr></thead><tbody><tr><td id="d317654e151">

**Connection Name**

</td><td>

Name of your Datadog connection. This name helps you identify it later. For example, `Datadog analysis AI agent connection`.

</td></tr><tr><td id="d317654e168">

**Connection URL**

</td><td>

URL of your Datadog instance. Datadog URLs follow this format: `https://api.datadoghq.com`.

</td></tr><tr><td id="d317654e186">

**Datadog API key**

</td><td>

Your Datadog API key.

</td></tr><tr><td id="d317654e200">

**Datadog Application key**

</td><td>

Your Datadog application key.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Datadog analysis AI agent to use it in the manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Datadog analysis AI agent, and turn on the agent in the Select channels and status screen.

To learn more about using the Datadog analysis AI agent in the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](../concept/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configuring agents and skills for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

**Related topics**  


[Configure the Dynatrace analysis AI agent](now-assist-itom-config-dynatrace.md)

[Configure the Google Gemini Cloud Assist agent](now-assist-itom-config-google-cloud.md)

[Configure the Kentik analysis AI agent](now-assist-itom-config-kentik.md)

[Configure the New Relic analysis AI agent](now-assist-itom-config-new-relic.md)

[Configure the manage alerts autonomously agentic workflow](configure-manage-alerts-autonomously-workflow.md)

