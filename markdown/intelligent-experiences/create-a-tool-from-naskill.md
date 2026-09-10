---
title: Create a tool from an AI skill
description: Create a tool from a generative AI skill to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-a-tool-from-naskill.html
release: zurich
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
breadcrumb: [Creating tools, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from an AI skill

Create a tool from a generative AI skill to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

## About this task

Prebuilt and custom AI skills are organized as governed MCP tools, enabling seamless discovery and accessibility for any standards-conforming MCP client. This structure enhances usability and encourages effective integration of these skills across various platforms. See [Generative AI skill support in MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-support-mcp.md) to learn about the pre-configured Now Assist skills.

**Note:** Only AI skills that don't rely on internal information as inputs, such as sys\_ids, are available to be created as tools. For more information about why a skill might not be available for creation as a tool, see the [AI Skill Eligibility Criteria for MCP Tool Integration \[KB2952564\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2952564) article in the Now Support Knowledge Base.

## Procedure

1.  Select AI skill from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Tool creation

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-naskill.png"\] Alt text: Create tool from Now Assist skill

    **Note:** The **category** is auto-populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI skill

</td><td>

Select an AI skill type from the list.

</td></tr><tr><td>

Label

</td><td>

An internal name for the tool.

</td></tr><tr><td>

MCP app

</td><td>

An active MCP app linked to this tool.

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


**Note:** If you add inputs to an AI skill definition after a tool has been created for the skill, you must create another tool to include the additional inputs and replace the existing tool.

## What to do next

Configure clients to connect to the server and use the tool. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md).

**Parent Topic:**[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-tools-mcp-server.md)

