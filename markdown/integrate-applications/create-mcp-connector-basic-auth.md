---
title: Create an MCP Connector with Basic Authentication
description: Create an MCP Connector with Basic Authentication for connecting to external systems or applications that support MCP.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Create an MCP Connector with Basic Authentication

Create an MCP Connector with Basic Authentication for connecting to external systems or applications that support MCP.

## Before you begin

Role required: sn\_mcp\_client.admin

## About this task

Use Basic Authentication when your MCP server requires a username and password for access. Ensure that valid server credentials are available before configuring the connector.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Select **Connectors**.

3.  Click **Create** and select **Model Context Protocol Connector**.

4.  On the form, fill in the fields.

<table id="table_system_details_basicauth"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server name

</td><td>

Name of the MCP server. For example, *Figma MCP server*.

</td></tr><tr><td>

System

</td><td>

Search for the external system you want to integrate.

</td></tr><tr><td>

Add system \(Optional\)

</td><td>

Click the ![Plus icon.](../../../product/rpa-hub/image/icon-plus.png) icon to add an external system. For more information, see [Create external systems](../../../build/workflow-data-fabric/task/connecthub-create-external-systems.md#).**Note:** If you already have an existing system, you can use that system for the MCP connector.

</td></tr><tr><td>

Connection name

</td><td>

Select **New connection** and enter a name to uniquely identify the connection. For example, *Figma Connection*.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Endpoint name|This field is auto-populated with the Connection name.|
    |Endpoint URL|Connection URL for the MCP server.|
    |Authentication Method|Select **Basic Authentication**.|
    |User name|User name of the MCP server.|
    |Password|Password of the MCP server.|

5.  Click **Save**.

    You are redirected to the third-party page requesting authorization for the MCP client.

6.  Click **Approve**.

    The MCP client for your application is created and appears in the **Model Context Protocol** list.


