---
title: Register via AI Agent Studio
description: Registering MCP servers via AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-register-mcp-servers-via-ai-agent-studio.html
release: zurich
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Configure agents to use MCP servers, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Register via AI Agent Studio

Registering MCP servers via AI Agent Studio.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Workspace** &gt; **AI Agent Studio**.

2.  Open the agent that uses the MCP server.

3.  Select **Edit**.

4.  Select **Tools**.

5.  Select the MCP server tool you want to update.

6.  Update the connection configuration:

    1.  Enter the Server URL.

    2.  Enter the Client ID.

    3.  Enter the Client secret.

    4.  Enter the Authentication endpoint URL

    5.  Enter the Token endpoint URL.

7.  Select **Save**.


## Result

The agent now connects to the MCP server through AI Gateway instead of directly. All requests are routed through AI Gateway, ensuring consistent policy enforcement across your AI ecosystem.

