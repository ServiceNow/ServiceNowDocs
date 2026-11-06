---
title: Create a tool from a Playbook
description: Create a tool from a Playbook to expose it to Model Context Protocol \(MCP\) clients from an MCP Server Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/create-a-tool-from-a-playbook.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [Create tool from search]
breadcrumb: [Creating tools, Configure, MCP Server Console, Extending AI with external systems and providers, Enable AI Experiences]
---

# Create a tool from a Playbook

Create a tool from a Playbook to expose it to Model Context Protocol \(MCP\) clients from an MCP Server Console.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

Minimum version required is Australia patch 6 or Brazil patch 1.

## Procedure

1.  Select Playbook from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Create tool from Playbook

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-playbook.png"\] Alt text: Form to create tool from Playbook

    **Note:** The **category** is automatically populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook

</td><td>

Select a compatible playbook from the list, that you want to add to the tool. If you're unable to see a playbook in the list, verify that the playbook is compatible.

</td></tr><tr><td>

Label

</td><td>

Add an internal name for the tool.

</td></tr><tr><td>

Description

</td><td>

The description of what the tool intends to do. This input is exposed to AI clients and used to determine when to call this tool.

**Note:** Add a specific, action-oriented description so AI clients can determine when to invoke the particular playbook.

</td></tr><tr><td>

MCP Servers

</td><td>

From the `MCP Servers` list, select a sever to which you want to add the tool. The AI clients will use the selected server to access the tool.

</td></tr></tbody>
</table>    **Note:** A tool can be used by multiple servers so any changes that you make to a tool apply to all servers that use the tool. Before editing a tool, review which servers it's associated with to determine the impact for every server.

    In the Tool inputs section, the fields associated with the capability are added.

3.  You can proceed with default configurations, only.

4.  Within the Tool inputs section, in the Enabled column, add the following two actions as tools to the MCP server.

    1.  Check Playbook Status

    2.  Check Playbook Execution

        **Note:** These Actions are available by default in the `Action` category. You must add these Actions and enable them in the tools list. Some tool inputs are required and can't be turned off.

5.  Select **Create**.


## What to do next

Invoke the tool using an MCP client and verify that it works as expected. Launch MCP client to test end-to-end execution. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/connect-mcp-server-client.md).

See [Playbooks as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-as-mcp-tool.md) to learn more.

**Parent Topic:**[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/creating-tools-mcp-server.md)

