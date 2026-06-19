---
title: Create a tool from Now Assist skill
description: Create a tool from Now Assist skills to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/create-a-tool-from-naskill.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Create a tool, Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool from Now Assist skill

Create a tool from Now Assist skills to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.

## Before you begin

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

Prebuilt and custom Now Assist skills are organized as governed MCP tools, enabling seamless discovery and accessibility for any standards-conforming MCP client. This structure enhances usability and encourages effective integration of these skills across various platforms. See [Now Assist skill support in MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-skill-support-mcp.md) to learn about the pre-configured Now Assist skills.

## Procedure

1.  Select Now Assist skill from these categories.

    \[Omitted image "mcp-create-tool-moveworks.png"\] Alt text: Tool creation

2.  On the form, fill in the fields.

    \[Omitted image "mcp-server-create-tool-naskill.png"\] Alt text: Create tool from Now Assist skill

    **Note:** The **category** is auto-populated if selected in the last modal.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Now Assist skill

</td><td>

Select a Now Assist skill type from the list.

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
</table>    In the Tool inputs section, the fields associated with the capability are added. See [Create a tool for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/create-tool-mcp-server.md) to learn more. The tool is now published on the MCP Servers and discoverable by MCP clients.


