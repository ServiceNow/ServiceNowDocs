---
title: Add an MCP server from AI Agent Studio
description: When you add an MCP server in AI Agent Studio, it's automatically discovered and synced to AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-an-mcp-server-from-ai-agent-studio.html
release: australia
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [MCP server setup, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from AI Agent Studio

When you add an MCP server in AI Agent Studio, it's automatically discovered and synced to AI Control Tower.

## Before you begin

Role required: sn\_aia.admin, sn\_mcp\_client.admin

**Note:** The AI Steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Manage MCP servers**.

2.  Select **New**.

    **Note:** In the Create and manage tab of the AI Agent studio, you can add only those MCP servers that have been approved in the AI Control Tower.

3.  Enter the Name.

4.  Select the Authentication type: OAuth 2.1.

    **Note:** AI Gateway supports OAuth 2.1.

5.  Select **Next**.

6.  Select the **Client registration type**: Dynamic client registration.

    AI Gateway registration in AI Agent Studio supports Dynamic Client Registration.

    When the server allows dynamic client registration, it will automatically retrieve the necessary details. Otherwise, you will need to enter the details manually.

7.  Select the **Grant type**.

8.  Select **Add**.

    The server gets added and displays the details of the server.

9.  Select **Authenticate** to authenticate the server with your credentials.

10. Select **Save**.

    **Note:** A scheduled job named **AI Agent Studio to AICT-MCP server sync** runs every 15 minutes to synchronize the MCP servers from AI Agent Studio to AI Control Tower.


## Result

After synchronizing, the MCP server shows up in the AI asset inventory with its Status listed as In review, and the lifecycle phase listed as New.

**Note:** After the MCP server is added to the AI Control Tower, it can’t be added again. Additionally, AI Agent Studio will not discover a server that has already been added.

## What to do next

MCP server approval workflow.

