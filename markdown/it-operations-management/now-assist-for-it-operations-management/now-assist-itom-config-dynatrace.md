---
title: Configure the Dynatrace analysis AI agent
description: Configure the Dynatrace analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow. After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-dynatrace.html
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure the manage alerts autonomously agentic workflow, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Dynatrace analysis AI agent

Configure the Dynatrace analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow.After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.

## Before you begin

**Important:** In the Australia release, the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent in AI Agent Studio and set up the Dynatrace MCP server agent. See [Configure observability agents for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md) for configuration details.

Before configuring the Dynatrace analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).
-   [Integrate Dynatrace platform events with Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/dynatrace-events-integration.md).
-   Copy your Dynatrace connection URL and Dynatrace access token or personal access token.

    The Dynatrace access token or personal access token must have the `problems.read` scope.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Dynatrace analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d287836e198">

Field

</th><th align="left" id="d287836e201">

Description

</th></tr></thead><tbody><tr><td id="d287836e207">

**Connection Name**

</td><td>

Name of your Dynatrace connection. This name helps you identify it later. For example, `Dynatrace analysis AI agent connection`.

</td></tr><tr><td id="d287836e224">

**Connection URL**

</td><td>

URL of your Dynatrace instance. Dynatrace URLs follow this format: `https://<your-resource-name>.live.dynatrace.com`.

</td></tr><tr><td id="d287836e242">

**Access token or personal access token \(must prefix with 'Api-Token '\)**

</td><td>

Dynatrace access token or personal access token. The token must begin with `Api-Token`, for example, `Api-Token dt0s01.STABCDEF12345.G3HIJKLMNOP`.

</td></tr><tr><td id="d287836e259">

**Header Name**

</td><td>

Header name for the Dynatrace platform token: `Authorization`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Dynatrace analysis AI agent to use it in the analyze alert impact agentic workflow or manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Dynatrace analysis AI agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the Dynatrace analysis AI agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about using the Dynatrace analysis AI agent in the analyze alert impact agentic workflow or manage alerts autonomously agentic workflow, see [Analyze alert impact in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-use-aia.md) and [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.md)

