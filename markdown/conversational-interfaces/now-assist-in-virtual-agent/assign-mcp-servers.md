---
title: Assign Model Context Protocol \(MCP\) servers to an assistant
description: Assign configured Model Context Protocol \(MCP\) servers to enable users to access external data sources and tools. You can assign an MCP server to an assistant that uses premium chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/assign-mcp-servers.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 2
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Assign Model Context Protocol \(MCP\) servers to an assistant

Assign configured Model Context Protocol \(MCP\) servers to enable users to access external data sources and tools. You can assign an MCP server to an assistant that uses premium chat.

## Before you begin

See [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-kg-schema-assistant.md).

Before assigning an MCP server to an assistant, make sure that the MCP server is created and available on the instance. For more information, see [Adding an MCP Server in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-mcp-client-on-ai-agent-studio.md).

Role required: virtual\_agent\_admin or admin

## About this task

Control which MCP servers are available to an assistant. After an MCP server is configured in AI Agent Studio, you can assign it to an assistant.

MCP server assignments are configured at the assistant level. This lets you control which assistants can use specific MCP servers, and which users can access MCP-provided capabilities through each assistant. An assistant can only use the MCP servers that are assigned to it.

**Note:** By default, no MCP servers are added, and you can save and continue without adding an MCP server.

## Procedure

1.  Select the **Add MCP server** drop-down list to add an MCP server to your assistant.

    \[Omitted image "sno-mcp-0826.png"\] Alt text: Select an MCP server from the drop down list.

    A tool is a function made available through an MCP server that allows an assistant to access data or perform a task on behalf of the user. If an MCP server doesn’t contain any tools, then the MCP server isn’t available for selection.

    After selecting an MCP server, the server shows in the list.

    \[Omitted image "sno-mcp-server-092026.png"\] Alt text: List of MCP servers and ability to edit.

    The **User access** column displays user access controls from AI Agent Studio.

    The **Tools** column shows the total number of tools for a server, regardless of permissions.

    The **Status** column shows whether a server is connected or if re-authentication is required.

    1.  Select the ellipsis to remove a server, authenticate, or manage a server's tool permissions. The MCP server modal is displayed.

        \[Omitted image "sno-mcp-server-modal-092026.png"\] Alt text: Manage tool permissions.

        -   The **Authenticate** button is used to authenticate to refresh tools. It's hidden if the MCP server uses an API key for authentication.
        -   Use **Search** to search for a tool.
        -   A list of tools shows their default or previously configured permissions.
        -   Tool permissions can be changed individually or as a bulk change by selecting **Set all permissions to**.
        -   The refresh button updates the list of tools shown in the table.
        After applying changes, remember to select **Save** or **Save and continue**.

    2.  Select **Manage MCP servers** to add an MCP server.
2.  Select **Save and continue**.


## What to do next

See [Add assets to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-assets.md).

