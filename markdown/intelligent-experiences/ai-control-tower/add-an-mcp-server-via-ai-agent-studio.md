---
title: Add an MCP server from ServiceNow AI Agent studio
description: Add an external MCP server from ServiceNow AI Agent studio.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 2
breadcrumb: [Process flow of MCP servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from ServiceNow AI Agent studio

Add an external MCP server from ServiceNow AI Agent studio.

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

    **Note:** In the Create and manage tab of the AI Agent studio, you can add only those MCP servers that have been approved in the AI Control Tower. To view these approvals, go to the Approvals tab on the MCP server record. For more information on Approvals tab and MCP server record, see [MCP server record](../concept/view-the-mcp-server-record.md)

3.  Enter the Name.

4.  Select the Authentication type: OAuth 2.1

    **Note:** AI Gateway supports OAuth 2.1.

5.  Select **Next**.

6.  Select the Client registration type: Dynamic Client Registration.

    AI Gateway registration in AI Agent Studio supports Dynamic Client Registration.

    If the server allows dynamic client registration, it will automatically retrieve the necessary details. Otherwise, you will need to enter the details manually.

7.  Select the **Grant type**.

8.  Select **Add**.

    The server gets added and displays the details of the server.

9.  Select **Authenticate** to authenticate the server with your credentials.

    **Note:** To view the approval request record for every MCP server in the AI Agent studio, click **View Approval record**. This action will direct you to the Related Variants tab of the respective MCP server

    To know more about Related Variants tab in the MCP server record, see [MCP server record](../concept/view-the-mcp-server-record.md)

10. Select **Save** to create an MCP server record.

    **Note:** A scheduled job named **AI Agent Studio to AICT-MCP server sync** runs every 15 minutes to synchronize the MCP servers from AI Agent Studio to AI Control Tower.


## Result

After synchronizing, the MCP server shows up in the AI asset inventory with its Status listed as In review, and the lifecycle phase listed as New.

**Note:** After the MCP server is added to the AI Control Tower, it can’t be added again. Additionally, AI Agent Studio will not discover a server that has already been added.

## What to do next

The MCP server approval request must be approved. See [MCP server approval workflow](playbook-workflow-of-mcp-server-approval-request.md)

