---
title: Create a tool from a REST API
description: Use a REST API to create a tool and expose it to Model Context Protocol \(MCP Server Console\) clients from an MCP Server Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-a-tool-from-rest-api.html
release: brazil
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Creating tools, Configure, MCP Server Console, Extending AI with external systems and providers, Enable AI Experiences]
---

# Create a tool from a REST API

Use a REST API to create a tool and expose it to Model Context Protocol \(MCP Server Console\) clients from an MCP Server Console.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

## Procedure

1.  Select REST API from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Tool category selection screen

2.  Complete the fields on the form.

    \[Omitted image "mcp-server-create-tool-restapi.png"\] Alt text: Create tool from REST APIs

    **Note:** The **Category** is auto-populated if selected in the previous dialog.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

REST API

</td><td>

REST API type for the tool.

</td></tr><tr><td>

Label

</td><td>

An internal name for the tool.

</td></tr><tr><td>

MCP app

</td><td>

An active MCP app linked to this REST API.

</td></tr><tr><td>

Description

</td><td>

The description of what the tool does. This input is exposed to AI clients and used to determine when to call this tool.

**Note:** Add a specific, action-oriented description. AI clients use it to decide when to invoke the tool.

 Client requests to Scripted REST API tools must include the inputs required by the API. The tool description must clearly state which inputs are required and what format they should be in so clients know exactly what to include in their request.

 For example, a well-written tool description could say: "Returns all open incidents assigned to a specified assignment group within a given date range. Requires: assignment\_group \(string, the exact group name\), start\_date \(string, format YYYY-MM-DD\), end\_date \(string, format YYYY-MM-DD\)." The calling agent uses this description to determine what to collect from the user before invoking the tool.

</td></tr><tr><td>

Annotations

</td><td>

Indication of the tool's behavior with MCP clients, including whether it only reads data, is idempotent, makes destructive changes or updates, or can call external links. You can also specifically combine these annotations as needed.

 The MCP client will use the selected annotations to categorize tools according to their behavior.

</td></tr><tr><td>

Required roles

</td><td>

One or more roles from the sys\_user\_role \[sys\_user\_role\] table that control access to the tool.

</td></tr><tr><td>

MCP Servers

</td><td>

One or more servers to add the tool to.

</td></tr></tbody>
</table>    **Note:** A tool can be used by multiple servers so any changes that you make to a tool apply to all servers that use the tool. Before editing a tool, review which servers it's associated with to determine the impact for every server.

    In the Tool inputs section, the fields associated with the capability are added.

3.  Turn off inputs from the tool that you don't want to expose.

    1.  In the Tool inputs section, locate the tool input.

    2.  From the Enabled column, select the toggle to turn off the input.

        **Note:** Some tool inputs are required and can't be turned off.

4.  Select **Create**.


## What to do next

Configure clients to connect to the server and use the tool. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/connect-mcp-server-client.md).

**Note:** When calling a Scripted REST API tool from a client, you must provide inputs in your request. If a required parameter, such as a record number, a date range, or a filter value, is not present in the request, the tool cannot complete the task.

**Parent Topic:**[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/creating-tools-mcp-server.md)

**Related topics**  


[Create a scripted REST API resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/t_CreateAScriptedRESTAPIResource.md)

