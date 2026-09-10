---
title: Activate SPO MCP Server
description: Activate the SPO MCP Server to make sourcing and procurement tools available to connected MCP clients on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/activate-spo-mcp-server.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [SPO MCP Server]
breadcrumb: [Use SPO MCP Server, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Activate SPO MCP Server

Activate the SPO MCP Server to make sourcing and procurement tools available to connected MCP clients on your ServiceNow instance.

## Before you begin

The following plugins must be activated on your instance:

-   ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) \(sn\_spend\_gen\_ai\)
-   Model Context Protocol Server \(sn\_mcp\_server\)

Role required: sn\_mcp\_server.admin or admin

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the **Configuration** tab, select **Servers**.

3.  Select **SPO MCP Server**.

4.  Change the application scope to **SPO MCP Server**.

    The **SPO MCP Server Console** page opens with all fields populated by default.

5.  From the **Deactivate** list, select **Activate**.

    All tools are available to connected MCP clients. For information about the available tools, see [SPO MCP Server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-mcp-server-tools-reference.md).

6.  Set up OAuth to authenticate SPO MCP Server with your ServiceNow instance.

<table id="table_e31_g5g_jkc"><thead><tr><th>

Authentication option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Use the SPO MCP Server OAuth client entry

</td><td>

1.  Select **Set up OAuth**.
2.  Navigate to the **sn\_spend\_gen\_ai.spo\_mcp\_server** client. The fields on the authorization code grant page are automatically populated.
3.  From the **Auth scope** list, select **a2aauthscope**.
4.  Select **Save**.


</td></tr><tr><td>

Set up your own OAuth connection

</td><td>

To set up your own OAuth client entry, the oauth\_admin or admin role is required. For more information on how to set up your own OAuth connection, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md).

</td></tr></tbody>
</table>
## Result

SPO MCP Server is activated and authenticated. Connected MCP clients can access all available sourcing and procurement tools.

