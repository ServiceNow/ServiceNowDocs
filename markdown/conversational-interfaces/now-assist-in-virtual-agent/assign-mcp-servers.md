---
title: Assign Model Context Protocol \(MCP\) servers to an assistant
description: Assign configured Model Context Protocol \(MCP\) servers to enable users to access external data sources and tools. Assigning an MCP server to an assistant is only available when using premium chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/assign-mcp-servers.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 1
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Assign Model Context Protocol \(MCP\) servers to an assistant

Assign configured Model Context Protocol \(MCP\) servers to enable users to access external data sources and tools. Assigning an MCP server to an assistant is only available when using premium chat.

## Before you begin

See [Add a Knowledge Graph schema to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-kg-schema-assistant.md).

Before assigning an MCP server to an assistant, make sure that:

-   The MCP server is created and available on the instance. For more information, see Add an MCP server in AI Agent Studio.
-   You know which users or roles should have access to the MCP-provided capabilities through the assistant.

Role required: virtual\_agent\_admin or admin

## About this task

Control which MCP servers are available to an assistant. After an MCP server is configured in AI Agent Studio, you can assign it to an assistant and configure role-based access for that assignment.

MCP server assignments are configured at the assistant level. This lets you control which assistants can use specific MCP servers, and which users can access MCP-provided capabilities through each assistant. An assistant can only use the MCP servers that are assigned to it.

## Procedure

1.  Select the **Add MCP server** drop-down list to add an MCP server to your assistant.

    \[Omitted image "sno-mcp-0826.png"\] Alt text: Select an MCP server from the drop down list.

    Upon selection of an MCP server, the server populates in the list.

    \[Omitted image "sno-mcp-edit-0826.png"\] Alt text: Edit or remove an MCP server by selecting the ellipsis.

    1.  Select the ellipsis to add, edit, or remove a role.

        \[Omitted image "sno-mcp-add-roles-0826.png"\] Alt text: Add roles.

        If roles aren't added, then all roles can access the specific MCP server.

    2.  Select **Manage MCP servers** to add an MCP server.
2.  Select **Save and continue**.


## What to do next

See [Add assets to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-assets.md).

