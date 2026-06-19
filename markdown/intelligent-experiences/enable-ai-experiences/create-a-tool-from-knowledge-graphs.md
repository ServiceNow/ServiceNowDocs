---
title: Create a tool from Knowledge Graph
description: Create a tool from Knowledge Graph to expose it to Model Context Protocol \(MCP\) clients from an MCP Server. Knowledge Graph provides agents with accurate, relationship-aware access to live instance data. This enables more precise, context-aware responses in every workflow by directly querying relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/create-a-tool-from-knowledge-graphs.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 1
keywords: [Create tool Knowledge graph for MCP]
breadcrumb: [Create a tool, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from Knowledge Graph

Create a tool from Knowledge Graph to expose it to Model Context Protocol \(MCP\) clients from an MCP Server. Knowledge Graph provides agents with accurate, relationship-aware access to live instance data. This enables more precise, context-aware responses in every workflow by directly querying relationships.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

See [Exploring Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/knowledge-graph/exploring-knowledge-graph.md) to explore Enterprise graphs and learn about creating Knowledge Graph.

## Procedure

1.  Select Knowledge Graph from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Tool creation

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-kg.png"\] Alt text: Create tool from Knowledge graph

    **Note:** The **category** is auto-populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Graph

</td><td>

Select a Knowledge Graph type from the list. You can either choose Enterprise Graph or one of the custom graphs.

</td></tr><tr><td>

Label

</td><td>

An internal name for the tool.

</td></tr><tr><td>

Description

</td><td>

The description of what the tool intends to do. This input is exposed to AI clients and used to determine when to call this tool.

**Note:** Admins must add specific and action-oriented description as the AI clients access it to decide when to invoke the tool.

</td></tr><tr><td>

MCP Servers

</td><td>

One or more servers you want to add your tool to.

</td></tr></tbody>
</table>    In the Tool inputs section, the fields associated with the capability are added. \[Omitted image "mcp-server-create-tool-kg-toolinput.png"\] Alt text: Tool input for Knowledge graph

    -   anchortables: Use one or more table names to make your query more specific. This is helpful when you know which tables are relevant to your question.
    -   tags: Include one or more tags to prioritize a specific group of tables. For example, you can use tags like 'CSM', 'HR'. These tags are required for the Enterprise Graph.
    -   description: Your query or request that will use Knowledge Graph.
    -   apioptions
    See [Create a tool for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/create-tool-mcp-server.md) to learn more. The tool is now published on the MCP Server and discoverable by MCP clients.


