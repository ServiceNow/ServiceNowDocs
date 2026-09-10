---
title: Add an MCP Server with API Key
description: Add an MCP Server with an API Key in the AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-mcp-server-api-key-new.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adding an MCP Server Console in AI Agent Studio, Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Add an MCP Server with API Key

Add an MCP Server with an API Key in the AI Agent Studio.

## Before you begin

Role required: sn\_mcp\_client.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Manage Model Contextual Protocol \(MSCP\) Servers**.

2.  Select **View** against **MCP Servers**.

3.  On the Model Context Protocol Server page, select **New**.

4.  On the form, fill in the fields.

    \[Omitted image "add-mcp-api-key.png"\] Alt text: Adding an MCP Server in AI Agent Studio with a API Key.

<table id="table_jnr_n3g_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your MCP Server.

</td></tr><tr><td>

Authentication Type

</td><td>

The authentication type with which you want to add your MCP Server.Select **API Key**.

</td></tr><tr><td>

MCP Server URL

</td><td>

The web address of your MCP Server.

</td></tr><tr><td>

API Key

</td><td>

A unique code or password to identify and authenticate the user or application when accessing the API.**Note:** The API Key adds a Connection alias dynamically at runtime and maps with the MCP Server.

</td></tr></tbody>
</table>5.  Select **Add**.

    You're redirected to the Model Context Protocol Server Console record to complete the Server details, Access rules, and Tools information.

6.  Verify the Server details.

    The Server name, Connection Alias, and Application fields are auto-populated with the information from previous steps. Additionally, you can provide a description for the server.

7.  Define Security controls for the MCP Servers.

    For more information, see [Define security controls for MCP Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-mcp.md).

8.  Define the Tools for the Model Context Protocol Sever.

    You can configure the MCP tools in the Assistant Designer. For more information see [Assign Model Context Protocol \(MCP\) servers to an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/assign-mcp-servers.md).

9.  Select **Save**.


## Result

An MCP Server Console with API Key authentication gets created with the name you provided and appears in the list of MCP Servers.

