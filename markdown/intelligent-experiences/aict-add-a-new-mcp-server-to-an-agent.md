---
title: Register an MCP server via AI Control Tower
description: When MCP Servers are registered through AI Control Tower, connecting them to an agent happens in two steps: first register the server at the instance level in AI Agent Studio, then add it as a tool within the specific agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-add-a-new-mcp-server-to-an-agent.html
release: zurich
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Configure agents to use MCP servers, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Register an MCP server via AI Control Tower

When MCP Servers are registered through AI Control Tower, connecting them to an agent happens in two steps: first register the server at the instance level in AI Agent Studio, then add it as a tool within the specific agent.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **AI Agent Studio**.

2.  Select **Settings**.

3.  Select **Manage MCP servers**.

4.  **New**.

5.  Enter the details:

    -   Name
    -   MCP server URL
    -   Authentication type
6.  Select **Next**.

7.  Create connection:

    1.  Select **Manual registration**.

    2.  Enter the following details:

        -   Grant type
        -   Token authentication method
        -   Client ID \(required\)
        -   Client secret
        -   Auth scopes
        -   Authorization URL \(required\)
        -   Token URL \(required\)
        -   Token Revocation URL
8.  Select **Submit**.

    **Note:** AI Control Tower doesn't sync credentials with AI Agent Studio automatically. You must copy credentials manually.

    The MCP Server is registered at the instance level in AI Agent Studio and is available for agents to use as a tool source.

9.  Add MCP sever as a tool in your agent:

    **Note:** Once the MCP server is registered in AI Agent Studio \(Phase 1\), add it to a specific agent as a tool.

    1.  Navigate to **AI Agent Studio**.

    2.  Open an existing agent or create a new agent.

    3.  Select **Edit**.

    4.  Select **Tools**.

    5.  Select **+ Add a tool**.

    6.  Select **+ New tool**.

    7.  Select **Model Context Protocol**.

    8.  Select the MCP server from the list.

        **Note:** In AWH for AI Control Tower \(2.0.0\), unapproved MCP Servers appear in the list but tools can't be fetched until the server is approved in AI Control Tower.

10. Select the specific tools from the MCP server that the agent should use.

11. Select **Save**.

    **Note:** Only approved MCP Servers can be added as tools in AI Agent Studio. If a server is not yet approved, a warning displays: Approval is needed to display tools. Check the MCP server record and contact your AI Steward


## Result

The MCP server is registered via AI Control Tower on a instance level and added it as a tool within the specific agent.

