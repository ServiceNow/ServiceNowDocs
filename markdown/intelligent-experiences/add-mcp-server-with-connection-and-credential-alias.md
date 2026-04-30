---
title: Add an MCP server with a connection and credential alias record
description: Add an MCP server by selecting a connection and credential alias record.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Add an MCP server in AI Agent Studio, Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP server with a connection and credential alias record

Add an MCP server by selecting a connection and credential alias record.

## Before you begin

A connection and credential alias record must be created.

For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Role required: sn\_mcp\_client.admin

## About this task

For authentication methods not supported in an MCP server, you can use the connection and credential alias method to create the alias manually and then update it in the MCP server. To use the OAuth-based authentication method, create the OAuth entity profile and then create the connection and credential alias. For other authentication methods like API key, Basic Auth, AWS Credentials, SSH Credentials, create the connection and credential alias directly.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to **Manage MCP Servers** and select **New**.

3.  In the **Authentication Type** field, select **Others**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for your MCP server.|
    |||
    |Connection and credential alias|Select a connection and credential alias record to map with your MCP server.|

    ![Screenshot that shows the Add MCP Server form and its fields.](../image/others-mcp-server.png)

5.  Select **Add**.

    **Note:** If a message appears that requires you to authenticate the MCP server, follow the message prompt.


## Result

An MCP server with the name you provided appears in the list of MCP servers.

