---
title: Connect Build Agent to a supported MCP server
description: Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Connect Build Agent to a supported MCP server

Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.

## Before you begin

The MCP connection must be configured before you connect to it in Build Agent. For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/model-context-protocol-connector.md).

The following MCP are currently supported for Build Agent:

-   Figma
-   Linear
-   Prisma

**Note:** MCP connections are currently available only in the ServiceNow IDE, not ServiceNow Studio.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  In the Build Agent chat panel, select the Settings icon ![](../image/ba-settings-icon.png).

    ![Build Agent panel showing greeting message and the Settings button](../image/ba-settings-panel-1.png "Build Agent panel with Settings icon")

3.  Select the **Enable MCP servers** toggle.

    ![Settings panel showing behavior and features configuration options with toggle switches](../image/ba-settings-panel-2.png "Enable MCP servers setting")

4.  Select the MCP servers icon ![](../image/ba-mcp-settings-icon.png) that appears after you enable MCP servers.

    ![Settings panel with the MCP settings button highlighted](../image/ba-mcp-settings-1.png "MCP settings icon")

5.  Select the **Connect** button for the MCP server you want to connect to.

    **Note:** You only need to connect to the MCP server once. After initial connection, the **Connect** button becomes a toggle for each available MCP server.

    The list of available MCP servers is inherited from the instance's registry.

    ![MCP settings showing MCP servers listed and a Connect button](../image/ba-mcp-list-1.png "Connect an MCP server")

6.  Select **Allow** in the confirmation dialog.


## Result

After Build Agent authenticates the connection, you can chat with it to ask questions related to the MCP server.

**Parent Topic:**[Configure Build Agent](configure-build-agent.md)

