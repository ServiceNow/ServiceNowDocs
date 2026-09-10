---
title: Create a Model Context Protocol server
description: Create a Model Context Protocol \(MCP\) server and configure which tools it exposes to MCP clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-mcp-server.html
release: australia
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create a Model Context Protocol server

Create a Model Context Protocol \(MCP\) server and configure which tools it exposes to MCP clients.

## Before you begin

Role required: sn\_mcp\_server.admin or admin

## About this task

Depending on your requirements, you can create servers that expose different tools for different use cases, such as for HR or IT workflows, or for different clients. You can also use the preconfigured Quickstart Server. For general guidelines on designing a server based on the job to be done, see the [Designing your first custom ServiceNow MCP server with MCP Server Console](https://www.servicenow.com/community/now-assist-articles/designing-your-first-custom-servicenow-mcp-server-with-mcp/ta-p/3566757) article in the ServiceNow Community.

Only stateless and remote servers are supported. Servers must be in the same application scope as any tools that they use.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console** or **Admin** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Servers**.

3.  Select **Create server**.

4.  On the form, fill in the fields.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

An internal name of your choice, for the server.

</td></tr><tr><td>

Name

</td><td>

An auto-created server name derived from the label you chose. This will be used in the URL endpoint. The server URL is created accordingly.

</td></tr><tr><td>

Application

</td><td>

The current application scope.**Note:** Servers must be in the same application scope as any tools that they use.

</td></tr><tr><td>

Short description

</td><td>

A description of the capabilities and purpose of the server.

</td></tr><tr><td>

Tools

</td><td>

The tools that the server exposes.

</td></tr></tbody>
</table>5.  From the Tools section, add the tools that the server exposes.

    1.  Select **Add tools**.

    2.  Search for tools from the list and select the tools to expose.

        The tool must be in the same application scope as the server. If you need to create a tool, select **Create tool**. For more information, see [Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/creating-tools-mcp-server.md).

    3.  Select **Add**.

6.  Select **Create** to make the server active.

    **Note:** To save your changes but not make the server active yet, select **Save as draft** instead. To activate it later, you can select **Activate** from the server record or the Servers page.

    After creating the server, the Server URL field is populated with the endpoint that you use to integrate with clients: `https://<instance>.service-now.com/sncapps/mcp-server/mcp/<server-name>`.

    If you need to turn off access to an existing server, select **Deactivate** from the server record or the Servers page.


## What to do next

Configure clients to connect to the server. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md).

**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

