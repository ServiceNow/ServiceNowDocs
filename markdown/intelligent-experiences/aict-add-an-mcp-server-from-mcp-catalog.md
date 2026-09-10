---
title: Add an MCP server from MCP Catalog
description: Add an MCP server from the MCP Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-add-an-mcp-server-from-mcp-catalog.html
release: zurich
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [MCP server setup, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from MCP Catalog

Add an MCP server from the MCP Catalog.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

**Note:** The AI Steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select **Add**.

3.  Select **Choose from MCP Catalog**.

4.  Search for a server using the search box, or browse available MCP servers displayed as cards with icons, descriptions, and versions.

5.  Select a server to view details including:

    -   MCP server URL
    -   Transport type \(HTTPS or SSE\)
    -   Available tools and capabilities
6.  Click **Select** to import the server.

    **Note:** The system auto-fills Name, MCP server URL, Authentication type, and Transport type.

    If the selected server supports CIMD \(Client Identity Metadata Document\), client registration details are also pre-filled automatically.

7.  Select **OK** to confirm your server and endpoint selections.

    **Note:** Add any additional details.

8.  Select **Submit**.

    The MCP server is submitted to AI Steward review.

    **Note:** You can only add one MCP server at a time. The MCP catalog only displays MCP servers that have not already been added to your instance.


## Result

The MCP server is added to AI Control Tower as an unmanaged asset with a lifecycle status of **In review**.

## What to do next

MCP server approval workflow.

