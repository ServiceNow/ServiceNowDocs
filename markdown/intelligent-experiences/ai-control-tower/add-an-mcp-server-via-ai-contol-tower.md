---
title: Add an MCP server from the AI Control Tower
description: Add an Model Context Protocol \(MCP\) server from the AI Control Tower.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from the AI Control Tower

Add an Model Context Protocol \(MCP\) server from the AI Control Tower.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

**Note:** The AI steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

For more information on the AI steward role and its responsibilities, see [AI Control Tower roles](../reference/roles-installed-with-ai-control-tower.md).

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select **Add**.

3.  Enter the Name \(Server name\).

4.  Enter the MCP server URL.

5.  Select **Next**.

6.  Select the Client registration type.

    **Note:** If you select Dynamic client Registration, the AI Control Tower automatically receives the Client ID and Client Secret. If you select Manual registration, the client must be created externally on the MCP provider side while the client ID and secret must be entered manually.

7.  Review all the other details such as the Grant type, and Token authentication method.

    **Note:** There are three sections for the URL:

    -   Authorization URL: Where the user authenticates and grants the access token
    -   Token URL: Where the system exchanges an authorization code for an access token
    -   Token revocation URL: Used to invalidate issued tokens if supported
8.  Select **Submit**.


## Result

The newly added MCP server is registered in the AI asset inventory MCP servers list and available for approval workflow.

