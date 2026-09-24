---
title: Add an MCP server from MCP Catalog
description: Add an MCP server from the MCP Catalog via AI Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-add-an-mcp-server-from-mcp-catalog.html
release: australia
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
keywords: [MCP server, MCP catalog, AI Gateway, MCP integration, MCP intake]
breadcrumb: [MCP server setup, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Add an MCP server from MCP Catalog

Add an MCP server from the MCP Catalog via AI Gateway.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

**Note:** The AI steward \(sn\_ai\_governance.ai\_steward\) role gets inherited with the following roles:

-   \(AI admin\) sn\_aia.admin
-   \(AIG admin\) aig\_admin
-   \(MCP Client admin\) sn\_mcp\_client.admin

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP Servers**.

2.  Select **Add**.

    Add MCP server page appears.

3.  Under Details, select **Choose from MCP Catalog**.

    **Note:**

    If you're unable to see any servers in the MCP Catalog during manual intake of MCP servers, perform the following procedure:

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    2.  Open Sync MCP Server Registry.

    3.  Select **Execute Now** to run the job manually.

        The MCP Catalog drop-down populates with the available MCP servers.

    **Note:**

    Run this job manually only if the MCP server catalog shows no records or fewer records than expected. By default, the job runs automatically on a schedule.

4.  Search for a server using the search box, or browse available MCP servers displayed as cards with icons, descriptions, and versions.

5.  Select a server to view details including:

    -   MCP server URL
    -   Transport type \(HTTPS or SSE\)
    -   Available tools and capabilities
    **Note:** SSE servers are visible in the MCP catalog, but AI Gateway does not support the SSE transport type. If you manually enter an SSE server in the intake form, the following warning message appears: “ SSE transport type was deprecated in the MCP specification in favor of Streamable HTTP and isn't supported by ServiceNow AI Gateway. Use the server's Streamable HTTP endpoint if available.”

6.  Click **Select** to import the server.

    **Note:** The system auto-fills Name, MCP server URL, Authentication type, and Transport type.

    If the selected server supports CIMD \(Client Identity Metadata Document\), client registration details are also pre-filled automatically.

7.  Select **OK** to confirm your server and endpoint selections.

8.  Select **Submit**.

    The MCP server is submitted for an AI Steward review.

    **Note:** You can only add one MCP server at a time. The MCP catalog only displays MCP servers that have not already been added to your instance.


## Result

The MCP server is added to AI Control Tower as an unmanaged asset with a lifecycle status of **In review**.

## What to do next

An AI Steward must review and approve the MCP server before it becomes available for use.

