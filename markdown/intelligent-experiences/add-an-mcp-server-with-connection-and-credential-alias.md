---
title: Add an MCP Server with Connection and Credential Alias
description: Add an MCP Server by selecting a Connection and Credential Alias record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adding an MCP Server in AI Agent Studio, Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP Server with Connection and Credential Alias

Add an MCP Server by selecting a Connection and Credential Alias record.

## Before you begin

-   Role required: sn\_mcp\_client.admin
-   Verify that you have a Connection and Credential alias record created before adding an MCP Server with Others as the option.

    For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).


## About this task

For using the Authentication methods not supported in MCP Server, you can use the Connection and Credential Alias method to create the Alias manually and then update it in the MCP Server. For using OAuth based authentication method, first create the OAuth entity profile and then create the Connection and Credential Alias. For other authentication methods like API Key, Basic Auth, AWS Credentials, SSH Credentials, create the connection and credential Alias directly.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to **Manage MCP Servers** and select **New**.

3.  On the form, fill in the fields.

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
</table>    ![Adding an MCP Server in AI Agent Studio with a Connection and credential alias record.](../image/others-mcp-server.png)

4.  Select **Add**.

    **Note:** Authenticate the MCP Server if you see the message requiring it.


## Result

An MCP Server with the name you provided appears in the list of MCP Servers.

