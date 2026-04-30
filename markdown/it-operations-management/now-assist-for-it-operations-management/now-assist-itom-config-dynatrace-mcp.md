---
title: Configure the Dynatrace MCP server agent
description: Configure the Dynatrace Model Context Protocol \(MCP\) server agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow. After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Dynatrace agents, Configuring agents and skills for Now Assist for ITOM, Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the Dynatrace MCP server agent

Configure the Dynatrace Model Context Protocol \(MCP\) server agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow. After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.

## Before you begin

Before configuring the Dynatrace MCP server agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   [Integrate Dynatrace platform events with Event Management](../../event-management/concept/dynatrace-events-integration.md).
-   Copy your Dynatrace connection URL.
-   Generate and copy a Dynatrace platform token.

    The Dynatrace platform token must be configured with the required permissions in Dynatrace. For more information, go to the [Dynatrace documentation](https://docs.dynatrace.com/docs) and see the "Dynatrace MCP server" page.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Dynatrace MCP server connection**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d134566e180">

Field

</th><th align="left" id="d134566e183">

Description

</th></tr></thead><tbody><tr><td id="d134566e189">

**Connection Name**

</td><td>

Name of your Dynatrace connection. This name helps you identify it later. For example, `Dynatrace MCP server connection`.

</td></tr><tr><td id="d134566e206">

**Connection URL**

</td><td>

URL of your Dynatrace instance. Dynatrace URLs follow this format: `https://<your-resource-name>.apps.dynatrace.com/platform-reserved/mcp-gateway/v0.1/servers/dynatrace-mcp/mcp`.

</td></tr><tr><td id="d134566e224">

**Platform token**

</td><td>

Dynatrace platform token. The token must begin with `Bearer`, for example, `Bearer dt0s01.STABCDEF12345.G3HIJKLMNOP`.

</td></tr><tr><td id="d134566e241">

**Header Name**

</td><td>

Header name for the Dynatrace platform token: `Authorization`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Dynatrace MCP server agent to use it in the analyze alert impact agentic workflow or manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Dynatrace MCP server agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the Dynatrace MCP server agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about the analyze alert impact agentic workflow or manage alerts autonomously agentic workflow, see [Use the analyze alert impact agentic workflow](now-assist-itom-use-aia.md) and [Manage alerts autonomously agentic workflow](../concept/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configuring Dynatrace agents](now-assist-itom-dynatrace-configs.md)

