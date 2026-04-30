---
title: Configure the Dynatrace analysis AI agent
description: Connect the Dynatrace analysis AI agent to your Dynatrace instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring AI agents for Now Assist for ITOM, Configuring Now Assist for IT Operations Management \(ITOM\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Configure the Dynatrace analysis AI agent

Connect the Dynatrace analysis AI agent to your Dynatrace instance to use it in the Analyze alert impact agentic workflow. Once connected, the AI agent gathers information to help you investigate alerts.

## Before you begin

Before configuring the Dynatrace analysis AI agent, you must do the following:

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   [Integrate Dynatrace platform events with Event Management](../../event-management/concept/dynatrace-events-integration.md).
-   Copy your Dynatrace connection URL and Dynatrace access token or personal access token.

    The Dynatrace access token or personal access token must have the `problems.read` scope.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Dynatrace analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

<table id="choicetable_uv4_x44_gfc"><thead><tr><th align="left" id="d269292e158">

Field

</th><th align="left" id="d269292e161">

Description

</th></tr></thead><tbody><tr><td id="d269292e167">

**Connection Name**

</td><td>

Name of your Dynatrace connection. This name helps you identify it later. For example, `Dynatrace analysis AI agent connection`.

</td></tr><tr><td id="d269292e184">

**Connection URL**

</td><td>

URL of your Dynatrace instance. Dynatrace URLs follow this format: `https://<your-resource-name>.live.dynatrace.com`.

</td></tr><tr><td id="d269292e202">

**Access token or personal access token \(must prefix with 'Api-Token '\)**

</td><td>

Dynatrace access token or personal access token. The token must begin with `Api-Token`, for example, `Api-Token dt0s01.STABCDEF12345.G3HIJKLMNOP`.

</td></tr><tr><td id="d269292e219">

**Header Name**

</td><td>

Header name for the Dynatrace platform token: `Authorization`. Change this value to customize the header for different APIs or follow specific security policies.

</td></tr></tbody>
</table>5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Dynatrace analysis AI agent to use it in the Analyze alert impact agentic workflow. In AI Agent Studio, navigate to Create and manage, find the Dynatrace analysis AI agent, and turn on the agent in the Define key requirements screen.

**Note:** While working in AI Agent Studio, make sure that the Alert information retrieval AI agent is active. It's also required for the Analyze alert impact agentic workflow.

To learn more about using the Dynatrace analysis AI agent in the Analyze alert impact agentic workflow, see [Use the Analyze alert impact agentic workflow](now-assist-itom-use-aia.md).

**Parent Topic:**[Configuring AI agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md)

