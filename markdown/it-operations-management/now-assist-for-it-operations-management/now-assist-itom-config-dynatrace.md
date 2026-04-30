---
title: Configure the Dynatrace analysis AI agent
description: Configure the Dynatrace analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow. After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Dynatrace agents, Configuring agents and skills for Now Assist for ITOM, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Dynatrace analysis AI agent

Configure the Dynatrace analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow.After you configure the agent, theworkflows can surface information from Dynatrace to help you investigate alerts.

## Before you begin

**Important:** Starting with Zurich Patch 7, the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent in AI Agent Studio and set up the Dynatrace MCP server agent. See [Configure the Dynatrace MCP server agent](now-assist-itom-config-dynatrace-mcp.md) for configuration details.

Before configuring the Dynatrace analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   [Integrate Dynatrace platform events with Event Management](../../event-management/concept/dynatrace-events-integration.md).
-   Copy your Dynatrace connection URL and Dynatrace access token or personal access token.

    The Dynatrace access token or personal access token must have the `problems.read` scope.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Dynatrace analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d480906e208">

Field

</th><th align="left" id="d480906e211">

Description

</th></tr></thead><tbody><tr><td id="d480906e217">

**Connection Name**

</td><td>

Name of your Dynatrace connection. This name helps you identify it later. For example, `Dynatrace analysis AI agent connection`.

</td></tr><tr><td id="d480906e234">

**Connection URL**

</td><td>

URL of your Dynatrace instance. Dynatrace URLs follow this format: `https://<your-resource-name>.live.dynatrace.com`.

</td></tr><tr><td id="d480906e252">

**Access token or personal access token \(must prefix with 'Api-Token '\)**

</td><td>

Dynatrace access token or personal access token. The token must begin with `Api-Token`, for example, `Api-Token dt0s01.STABCDEF12345.G3HIJKLMNOP`.

</td></tr><tr><td id="d480906e269">

**Header Name**

</td><td>

Header name for the Dynatrace platform token: `Authorization`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Dynatrace analysis AI agent to use it in the analyze alert impact agentic workflowor manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Dynatrace analysis AI agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the Dynatrace analysis AI agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about using the Dynatrace analysis AI agent in the analyze alert impact agentic workflowor manage alerts autonomously agentic workflow, see [Use the analyze alert impact agentic workflow](now-assist-itom-use-aia.md)and [Manage alerts autonomously agentic workflow](../concept/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configuring Dynatrace agents](now-assist-itom-dynatrace-configs.md)

