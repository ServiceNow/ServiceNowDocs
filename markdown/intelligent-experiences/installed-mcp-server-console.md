---
title: Components installed with MCP Server Console
description: Several types of components are installed with activation of the MCP Server Console application, including tables and user roles.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-15"
reading_time_minutes: 1
breadcrumb: [Reference, MCP Server Console, Enable AI experiences]
---

# Components installed with MCP Server Console

Several types of components are installed with activation of the MCP Server Console application, including tables and user roles.

## Roles installed

<table id="table_ifl_dgg_3gc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

MCP Server administrator

 \[sn\_mcp\_server.admin\]

</td><td>

Performs create, read, update, and delete \(CRUD\) operations on all MCP Server Console tables.

</td><td>

sn\_mcp\_server.tools\_admin

</td></tr><tr><td>

MCP Server tools administrator

 \[sn\_mcp\_server.tools\_admin\]

</td><td>

Performs create, read, update, and delete \(CRUD\) operations for tools.

</td><td>

-   canvas\_user
-   sn\_nowassist\_admin.user
-   web\_service\_admin

</td></tr><tr><td>

MCP Server viewer

 \[sn\_mcp\_server.viewer\]

</td><td>

Invokes tools and views all MCP Server Console tables \(read-only access\).

</td><td>

-   one\_extend\_viewer
-   canvas\_user
-   sn\_nowassist\_admin.user
-   web\_service\_admin

</td></tr></tbody>
</table>## Tables installed

<table id="table_mfl_dgg_3gc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Skill Tool Definition

 \[sn\_mcp\_ai\_skill\_tool\_definition\]

</td><td>

Tools based on Now Assist skills. Extends the Tool Definition table.

</td></tr><tr><td>

AI Skill Tool Input

 \[sn\_mcp\_ai\_skill\_tool\_input\]

</td><td>

Inputs for tools based on Now Assist skills. Extends the Tool Input table.

</td></tr><tr><td>

Provisioned MCP Server

 \[sn\_mcp\_server\_registry\]

</td><td>

MCP servers deployed on the instance.

</td></tr><tr><td>

Scripted REST Tool Definition

 \[sn\_mcp\_scripted\_rest\_tool\_definition\]

</td><td>

Tools based on Scripted REST APIs that enable other tools. Extends the Tool Definition table.

</td></tr><tr><td>

Scripted REST Tool Input

 \[sn\_mcp\_scripted\_rest\_input\]

</td><td>

Inputs for tools based on Scripted REST APIs. Extends the Tool Input table.

</td></tr><tr><td>

Tool Definition

 \[sn\_mcp\_tool\_definition\]

</td><td>

Tools defined for use by MCP servers.

</td></tr><tr><td>

Tool Input

 \[sn\_mcp\_tool\_input\]

</td><td>

Inputs defined for use by MCP server tools.

</td></tr></tbody>
</table>**Parent Topic:**[MCP Server Console reference](../concept/mcp-server-console-reference.md)

