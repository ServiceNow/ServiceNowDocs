---
title: Install Model Context Protocol Client
description: Install the MCP Client application on your ServiceNow instance to enable using the tools from the MCP server in AI agents.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Install Model Context Protocol Client

Install the MCP Client application on your ServiceNow instance to enable using the tools from the MCP server in AI agents.

## Before you begin

The following must be completed:

-   The Generative AI Controller plugin \[com.sn.generative.ai\] is installed.

    **Note:** Installing the Generative AI Controller plugin enables AI Agent Studio and the MCP Client on your instance.

-   The latest version of the Now Assist AI Agents plugin \[sn\_aia\].
-   The **sn\_aia.enable\_mcp\_tool** system property is set to **true** to enable the MCP tool experience.

**Note:** ServiceNow AI Platform supports Protocol version 2025-06-18 of the MCP servers for MCP Client.

Role required: sn\_mcp\_client.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the Model Context Protocol Client plugin \[sn\_mcp\_client\].


