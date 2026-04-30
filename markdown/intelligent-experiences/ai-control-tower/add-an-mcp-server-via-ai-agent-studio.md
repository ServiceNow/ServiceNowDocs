---
title: Add an MCP server from AI Agent studio
description: Add an external MCP server from AI Agent studio.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP servers Via AI Gateway, Explore AI Gateway, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from AI Agent studio

Add an external MCP server from AI Agent studio.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

**Note:** The AI steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

For more information on the AI steward role and its responsibilities, see [AI Control Tower roles](../reference/roles-installed-with-ai-control-tower.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Manage MCP servers**.

2.  Select **New**.

3.  Enter the Name.

4.  Select the Authentication type: OAuth 2.1

    **Note:** AI Gateway supports OAuth 2.1.

5.  Select **Next**.

6.  Select the Client registration type: Dynamic Client Registration.

    AI Gateway registration in AI Agent Studio supports only Dynamic Client Registration.

    If the server allows dynamic client registration, it will automatically retrieve the necessary details. Otherwise, you will need to enter the details manually.

7.  Select the **Grant type**.

8.  Select **Add**.

    The server gets added and displays the details of the server.

9.  Select **Authenticate** to authenticate the server with your credentials.

10. Select **Save** to create an MCP server record.

    A scheduled job named **AI Agent Studio to AICT-MCP server sync** runs every 15 minutes to synchronize the MCP servers from AI Agent Studio to AI Control Tower.


## Result

After synchronizing, the MCP server shows up in the AI asset inventory with its Status listed as In review, and the lifecycle phase listed as New.

**Note:** After the MCP server is added to the AI Control Tower, it can’t be added again. Additionally, AI Agent Studio will not discover a server that has already been added.

## What to do next

The MCP server approval request must be approved. See [MCP server approval request](playbook-workflow-of-mcp-server-approval-request.md)

