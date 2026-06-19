---
title: Connect Build Agent to a supported MCP server
description: Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/ba-connct-mcp-server.html
release: australia
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Connect Build Agent to a supported MCP server

Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.

## Before you begin

Before you can enable an MCP server in Build Agent, an administrator must approve it as an AI asset in AI Control Tower. Each MCP server requires this approval, regardless of whether the server is enabled by default.

The end-to-end flow for making an MCP server available is:

1.  The administrator adds the MCP server as a Workflow Data Fabric \(WDF\) connection.
2.  The administrator approves the server as an AI asset in AI Control Tower.
3.  You authenticate the connection in Personal Integrations.
4.  You enable the MCP server in Build Agent settings.

Individual MCP servers are enabled by default, but the complete flow must be completed before any server is available for use.

For details on adding a new MCP connection in Workflow Data Fabric, see .

See [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/accelerate-design-to-development-with-figma-mcp-server.md) for a list of supported MCP servers.

**Note:** MCP connections are available in both ServiceNow Studio and the ServiceNow IDE, though you must be on Australia Patch 3 or higher to use MPC servers with Build Agent in ServiceNow Studio.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio** or **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  In the Build Agent chat panel, select the Settings icon \[Omitted image "ba-settings-icon.png"\] Alt text:.

    \[Omitted image "ba-settings-panel-1.png"\] Alt text: Build Agent panel showing greeting message and the Settings button

3.  Select the **Enable MCP servers** toggle.

    \[Omitted image "ba-settings-panel-2.png"\] Alt text: Settings panel showing behavior and features configuration options with toggle switches

4.  Select the MCP servers icon \[Omitted image "ba-mcp-settings-icon.png"\] Alt text: that appears after you enable MCP servers.

    \[Omitted image "ba-mcp-settings-1.png"\] Alt text: Settings panel with the MCP settings button highlighted

5.  Confirm that the MCP server you want is present and enabled.

    \[Omitted image "ba-mcp-list-enabled.png"\] Alt text: Build Agent panel showing MCP servers, all with toggles enabled.

    **Note:** If the MCP server you want isn't available, you must first set it up in Personal Integrations.

6.  Select **Allow** in the confirmation dialog.

    You must do this only for the initial connection.


## Result

After Build Agent authenticates the connection, you can chat with it to ask questions related to the MCP server.

**Parent Topic:**[Configure Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/configure-build-agent.md)

