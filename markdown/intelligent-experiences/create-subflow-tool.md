---
title: Create a tool from Subflow
description: Create a tool from Subflow to expose it to Model Context Protocol \(MCP\) clients from an MCP Server. Subflows and actions empower agents to complete tasks seamlessly —from submitting requests to routing for approval and confirming outcomes across workflows, without leaving the client interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-subflow-tool.html
release: zurich
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
keywords: [Create subflow tool type for MCP server]
breadcrumb: [Create a tool, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from Subflow

Create a tool from Subflow to expose it to Model Context Protocol \(MCP\) clients from an MCP Server. Subflows and actions empower agents to complete tasks seamlessly —from submitting requests to routing for approval and confirming outcomes across workflows, without leaving the client interface.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

Perform these steps before creating a tool:

1.  Create a subflow in Flow Designer using supported input and output data types. See [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/create-subflow.md) to learn more.
2.  Establish the requisite AI Access Control List \(ACL\) to facilitate external invocation of the component. See [Create AI ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-acl.md) to learn more.
3.  Confirm the compatibility status in the staging table. See [Check compatibility of Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/check-compatibility-of-subflow.md) to learn more.
4.  Register the component as a tool within the MCP Server.

## Procedure

1.  Select Subflow from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Tool creation

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-subflow.png"\] Alt text: Create tool from Subflow

    **Note:** The **category** is auto-populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subflow

</td><td>

Select a Subflow type from the list.

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
</table>    In the Tool inputs section, add the fields associated with the capability. See [Create a tool for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-tool-mcp-server.md) to learn more. The tool is now published on the MCP Server and discoverable by MCP clients.


## What to do next

Invoke the tool via Claude or an alternative MCP client and verify that it functions as intended. With the tool you registered, open your MCP client to test end-to-end execution.

