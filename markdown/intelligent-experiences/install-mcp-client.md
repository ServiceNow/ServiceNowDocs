---
title: Install Model Context Protocol Client
description: Install the MCP Client application on your ServiceNow instance to enable using the tools from the MCP Server in AI agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Install Model Context Protocol Client

Install the MCP Client application on your ServiceNow instance to enable using the tools from the MCP Server in AI agents.

## Before you begin

Role required: sn\_mcp\_client.admin

Verify that you:

-   Install the AI Agent Studio plugin \[com.snc.sn\_aia\] and the Generative AI Controller plugin \[com.sn.generative.ai\] to use the MCP Client.
-   Enable the MCP Tool experience in your instance by setting the **sn\_aia.enable\_mcp\_tool** system property to **true**.

**Note:** ServiceNow supports Protocol version 2025-03-26 of the MCP Servers for MCP Client.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for Model Context Protocol Client plugin \[sn\_mcp\_client\].

3.  Select **Install**.


