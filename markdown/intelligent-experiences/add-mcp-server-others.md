---
title: Add an MCP Server with Connection and Credential Alias
description: Add an MCP Server by selecting a Connection and Credential Alias record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-mcp-server-others.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Adding an MCP Server Console in AI Agent Studio, Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Add an MCP Server with Connection and Credential Alias

Add an MCP Server by selecting a Connection and Credential Alias record.

## Before you begin

-   Role required: sn\_mcp\_client.admin
-   Verify that you have a Connection and Credential alias record created before adding an MCP Server with Others as the option.

    For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md).


## About this task

To use authentication methods not supported in MCP Server, use the Connection and Credential Alias method. Create the alias manually and then update it in the MCP Server. For OAuth-based authentication, first create the OAuth entity profile. Then create the Connection and Credential Alias. For other authentication methods like API Key, Basic Auth, AWS Credentials, or SSH Credentials, create the connection and credential alias directly.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Manage Model Contextual Protocol \(MSCP\) Servers**.

2.  Select **View** against **MCP Servers**.

3.  On the Model Context Protocol Server page, select **New**.

4.  On the form, fill in the fields.

    \[Omitted image "add-mcp-server-other.png"\] Alt text: Adding an MCP Server in AI Agent Studio with a Connection and credential alias record.

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

The authentication type with which you want to add your MCP Server.Select **Others**.

</td></tr><tr><td>

Connection and credential alias

</td><td>

Select a Connection and credential alias record to map with your MCP Server.

</td></tr></tbody>
</table>5.  Select **Add**.

    You're redirected to the Model Context Protocol Server Console record to authenticate the MCP server for adding an MCP tool to an AI agent.

6.  Select **Save** and continue to complete filling the Server details, Access rules, and Tools.

7.  Verify the Server details.

    The Server name, Connection Alias, and Application fields are auto-populated with the information from previous steps. Additionally, you can provide a description for the server.

8.  Define Security controls for the MCP Servers.

    For more information, see [Define security controls for MCP Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-mcp.md).

9.  Define the Tools for the Model Context Protocol Sever.

    You can configure the MCP tools in the Assistant Designer. For more information see [Assign Model Context Protocol \(MCP\) servers to an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/assign-mcp-servers.md).

10. Select **Save**.

    **Note:** On the Model Context Protocol Server Console record, you will see a warning that server requires authentication. Authenticate the MCP Server if you see the message requiring it.


## Result

An MCP Server with the name you provided appears in the list of MCP Servers.

