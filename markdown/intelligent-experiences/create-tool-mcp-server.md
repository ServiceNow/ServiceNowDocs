---
title: Create a tool for a Model Context Protocol server
description: Create a tool from a Now Assist skill to expose it to Model Context Protocol \(MCP\) clients from an MCP server.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Create a tool for a Model Context Protocol server

Create a tool from a Now Assist skill to expose it to Model Context Protocol \(MCP\) clients from an MCP server.

## Before you begin

If you aren't using the Quickstart Server, create a server to which you can add tools. For more information, see [Create a Model Context Protocol server](create-mcp-server.md).

Role required: sn\_mcp\_server.tools\_admin, sn\_mcp\_server.admin, or admin

## About this task

Each server must include at least one tool.

-   Tools define which functionality and data a server exposes to clients and the actions that can be performed on an instance by clients. Tools are based on existing capabilities, such as Now Assist skills, including custom skills created with Now Assist Skill Kit. For a list of Now Assist skills that can be used as tools, see [Now Assist skill support in MCP Server Console](../reference/now-assist-skill-support-mcp.md).
-   Tools include inputs that correspond to the fields of the existing capability. Inputs that are enabled for a tool are exposed to clients.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Tools**.

3.  Select **Create tool**.

    1.  **Important:** The following tool type categories in addition to Now Assist skill, are currently enabled to be piloted Moveworks users only:

        Select a tool type you wish to create from these categories: Subflow, Action, Knowledge graph and scripted REST API.

        These tools can be added to Moveworks Quickstart Server only.

    2.  Perform rest of the following steps.

4.  On the form, fill in the fields.

<table id="table_l2y_lhm_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Now Assist skill

</td><td>

A Now Assist skill to use as a tool with servers.**Note:** The **category** is auto-populated if selected in the last modal.

</td></tr><tr><td>

Label

</td><td>

An internal name for the tool.

</td></tr><tr><td>

Description

</td><td>

A description of what the tool does and the inputs it exposes to clients. The description can be accessed from clients and used to determine when to call this tool.

</td></tr><tr><td>

Servers

</td><td>

One or more servers you want to add your tool to.

</td></tr></tbody>
</table>    In the Tool inputs section, the fields associated with the capability are added.

5.  Turn off inputs from the tool that you don't want to expose.

    1.  In the Tool inputs section, locate the tool input.

    2.  From the Enabled column, select the toggle to turn off the input.

        **Note:** Some tool inputs are required and can't be turned off.

6.  Select **Create**.


**Note:** If you add inputs to a Now Assist skill after a tool has been created, you must create another tool to include the additional inputs and replace the existing tool.

## What to do next

Configure clients to connect to the server and use the tool. For more information, see [Connecting to an MCP server from an MCP client](../concept/connect-mcp-server-client.md#).

**Related topics**  


[Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md)

[Now Assist Skill Kit](../../now-assist-skill-kit/concept/now-assist-skill-kit-landing.md)

