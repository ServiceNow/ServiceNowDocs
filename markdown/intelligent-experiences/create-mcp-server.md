---
title: Create a Model Context Protocol server
description: Create a Model Context Protocol \(MCP\) server and configure which tools it exposes to MCP clients.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create a Model Context Protocol server

Create a Model Context Protocol \(MCP\) server and configure which tools it exposes to MCP clients.

## Before you begin

Role required: sn\_mcp\_server.admin or admin

## About this task

Depending on your requirements, you can create one or more servers that expose different tools for different use cases, such as for HR or IT workflows, or for different clients. You can also use the preconfigured Quickstart Server.

This page also provides explore search, refresh and many other page view options.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Servers**.

3.  Select **Create server**.

    ![Create server for MCP client](../image/mcp-create-server.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|An internal name of your choice, for the server.|
    |Name|An auto-created server name derived from the label you chose. This will be used in the URL endpoint. The server URL is created accordingly.|
    |Short description|A description of the capabilities and purpose of the server.|
    |Tools|The tools that the server exposes.|

5.  From the Tools section, add the tools that the server exposes.

    1.  Select **Add tools**.

    2.  Search for tools from the list and select the tools to expose.

        If you need to create a tool, select **Create tool**. For more information, see [Create a tool for a Model Context Protocol server](create-tool-mcp-server.md).

    3.  Select **Add**.

6.  Select **Create** to make the server active.

    **Note:** To save your changes but not make the server active yet, select **Save as draft** instead. To activate it later, you can select **Activate** from the server record or the Servers page.

    After creating the server, the Server URL field is populated with the endpoint that you use to integrate with clients: `https://<instance>.service-now.com/sncapps/mcp-server/mcp/<server-name>`.

    If you need to turn off access to an existing server, select **Deactivate** from the server record or the Servers page.


## What to do next

Configure clients to connect to the server. For more information, see [Connecting to an MCP server from an MCP client](../concept/connect-mcp-server-client.md#).

