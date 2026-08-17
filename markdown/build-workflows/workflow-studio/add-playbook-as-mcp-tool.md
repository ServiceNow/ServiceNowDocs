---
title: Add a playbook as an MCP tool
description: Create a tool in the MCP Server Console and expose it in an MCP server so that MCP clients can invoke the playbook through the MCP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/add-playbook-as-mcp-tool.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbooks as an MCP tool, Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add a playbook as an MCP tool

Create a tool in the MCP Server Console and expose it in an MCP server so that MCP clients can invoke the playbook through the MCP.

## Before you begin

Make sure you have an existing MCP server to which you want to add the playbook as a tool. For more information, see [Create an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-mcp-server.md)

Create or update existing playbooks to make sure that they are compatible for exposing as an MCP tool. For more information, see [Playbooks as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-as-mcp-tool.md).

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Tools**.

3.  Select **Create tool**.

4.  Select the **Playbook** category.

    \[Omitted image "mcp-tool-playbook.png"\] Alt text: Options to select categories for MCP server tool.

5.  Fill in the following information.

    \[Omitted image "create-playbook-tool.png"\] Alt text: Fill in the fields to create a playbook MCP tool.

    -   **Playbook**: From the list of compatible playbooks, select the playbook that you want to add to the tool.
    -   **Label**: Add an internal name for the tool.
    -   **Description**: Provide a description of what the tool intends to do. This input is exposed to AI clients and used to determine when to call this tool.

        **Note:** Add specific and action-oriented description as the AI clients access it to decide when to invoke the tool.

    -   **Active**: Select to make the tool active and ready for execution.
    -   From the **MCP Servers** list, select a sever to which you want to add the tool. The AI clients will use the selected server to access the tool.
6.  Review the tool inputs and modify if necessary.

7.  Select **Create**.

    The playbook is available as a tool in the MCP server. MCP clients connected to the server can invoke the playbook as part of an agentic workflow.


## What to do next

Configure clients to connect to the server and use the tool. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

**Parent Topic:**[Playbooks as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-as-mcp-tool.md)

