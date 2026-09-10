---
title: Add an MCP server from AI Control Tower
description: Add an MCP server manually from AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-add-an-mcp-server-from-ai-control-tower.html
release: zurich
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [MCP server setup, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from AI Control Tower

Add an MCP server manually from AI Control Tower.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

**Note:** The AI Steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select **Add**.

3.  Enter the Name \(Server name\).

4.  Enter the MCP server URL.

5.  Enter the Description \(Optional\).

6.  Enter the External MCP server documentation URL \(Optional\).

7.  Select the Provider from the list.

8.  Select the Vendor from the list.

9.  Select **Next**.

10. Select the **Client registration type**.

    **Note:** If you select Dynamic client registration, AI Control Tower automatically receives the Client ID and Client secret. If you select Manual registration, you must create the client externally on the MCP provider side and enter the Client ID and Client secret manually.

11. If you select Manual registration, review and complete the following details:

    -   Grant type
    -   Token authentication method
    -   Client ID
    -   Client secret
    -   Auth scopes
    -   Authorization URL
    -   Token URL
    -   Token revocation URL
12. Select **Submit**.


## Result

The MCP server is registered in the AI asset inventory as an unmanaged asset with a status of In review.

## What to do next

MCP server approval workflow.

