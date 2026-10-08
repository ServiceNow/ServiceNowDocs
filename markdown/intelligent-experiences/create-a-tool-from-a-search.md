---
title: Create a tool from a Search
description: Create a tool from a Search to expose it to Model Context Protocol \(MCP\) clients from an MCP Server Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/create-a-tool-from-a-search.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [Create tool from search]
breadcrumb: [Creating tools, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from a Search

Create a tool from a Search to expose it to Model Context Protocol \(MCP\) clients from an MCP Server Console.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

Minimum version required is Australia patch 6 or Brazil patch 0.

## Procedure

1.  Select Search from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Create tool from Search

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-search.png"\] Alt text: Create tool from Search

    **Note:** The **category** is automatically populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search

</td><td>

Select a search type from the list.

</td></tr><tr><td>

Label

</td><td>

An internal name for the tool.

</td></tr><tr><td>

MCP app

</td><td>

An active MCP app linked to this search profile.

</td></tr><tr><td>

Description

</td><td>

The description of what the tool intends to do. This input is exposed to AI clients and used to determine when to call this tool.

**Note:** Add a specific, action-oriented description so AI clients can determine when to invoke the tool.

</td></tr><tr><td>

Annotations

</td><td>

Indication of the tool's behavior with MCP clients, including whether it only reads data, is idempotent, makes destructive changes or updates, or can call external links. You can also specifically combine these annotations as needed.

 The MCP client uses the selected annotations to categorize tools according to their behavior.

</td></tr><tr><td>

MCP Servers

</td><td>

One or more servers to add the tool to.

</td></tr></tbody>
</table>    **Note:** A tool can be used by multiple servers so any changes that you make to a tool apply to all servers that use the tool. Before editing a tool, review which servers it's associated with to determine the impact for every server.

    In the Tool inputs section, the fields associated with the capability are added.

3.  You can proceed with default configurations, only.

    1.  In the Tool inputs section, locate the tool input.

    2.  From the Enabled column, select the toggle to turn off the input.

        **Note:** Some tool inputs are required and can't be turned off.

4.  Select **Create**.


## What to do next

Invoke the tool using an MCP client and verify that it works as expected. Launch MCP client to test end-to-end execution. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/connect-mcp-server-client.md).

**Parent Topic:**[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/creating-tools-mcp-server.md)

