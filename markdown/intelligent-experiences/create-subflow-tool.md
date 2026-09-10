---
title: Create a tool from a Subflow
description: Create a tool from a Subflow to expose it to Model Context \(MCP\) clients from an MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-subflow-tool.html
release: zurich
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [Create subflow tool type for MCP server]
breadcrumb: [Creating tools, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from a Subflow

Create a tool from a Subflow to expose it to Model Context \(MCP\) clients from an MCP Server.

## Before you begin

Perform these steps before creating a tool from a Subflow:

1.  Create a Subflow in Workflow Studio using supported input and output data types. See [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-subflow.md) to learn more.

    **Note:** Only synchronous Subflows are supported. Subflows with wait steps, asynchronous execution, or human intervention steps can't be used as tools.

2.  Establish the requisite AI Access Control List \(ACL\) to facilitate external invocation of the component. See [Create an AI ACL for a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-acl.md) to learn more.
3.  Confirm the compatibility status in the staging table. See [Check the compatibility of a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/check-compatibility-of-subflow.md) to learn more.

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

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

MCP app

</td><td>

An active MCP app linked to this subflow.

</td></tr><tr><td>

Description

</td><td>

The description of what the tool intends to do. This input is exposed to AI clients and used to determine when to call this tool.

**Note:** Admins must add specific and action-oriented description as the AI clients access it to decide when to invoke the tool.

</td></tr><tr><td>

Annotations

</td><td>

Indication of the tool's behavior with MCP clients, including whether it only reads data, is idempotent, makes destructive changes or updates, or can call external links. You can also specifically combine these annotations as needed.

 The MCP client will use the selected annotations to categorize tools according to their behavior.

</td></tr><tr><td>

MCP Servers

</td><td>

One or more servers you want to add your tool to.

</td></tr></tbody>
</table>    **Note:** A tool can be used by multiple servers so any changes that you make to a tool apply to all servers that use the tool. Before editing a tool, review which servers it's associated with to determine the impact for every server.

    In the Tool inputs section, the fields associated with the capability are added.

3.  Turn off inputs from the tool that you don't want to expose.

    1.  In the Tool inputs section, locate the tool input.

    2.  From the Enabled column, select the toggle to turn off the input.

        **Note:** Some tool inputs are required and can't be turned off.

4.  Select **Create**.


## What to do next

Invoke the tool via Claude or an alternative MCP client and verify that it functions as intended with the tool you registered. Launch MCP client to test end-to-end execution. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md).

**Parent Topic:**[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-tools-mcp-server.md)

