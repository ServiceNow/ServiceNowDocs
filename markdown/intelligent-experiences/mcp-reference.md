---
title: Model Context Protocol Client reference
description: Find more information about user roles, tables, and the different properties that are installed with the Model Context Protocol Client application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Model Context Protocol Client reference

Find more information about user roles, tables, and the different properties that are installed with the Model Context Protocol Client application.

## MCP Client roles

The following roles are installed with the Model Context Protocol Client plugin \[sn\_mcp\_client\].

<table id="table_j5p_st2_xfc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MCP Client Admin \[sn\_mcp\_client.admin\]

</td><td>

Administrator of the application.A user with the sn\_mcp-client.admin role can create, read, update, and delete records.

**Note:** The sn\_aia.admin role contains the sn\_mcp\_client.admin role, a role inheritance on plugin activation.

</td></tr><tr><td>

MCP Client Viewer \[sn\_mcp\_client.viewer\]

</td><td>

Read-only access to the application. A user with the sn\_mcp\_client.viewer role has read and report access on all tables.

**Note:** The sn\_aia.viewer role contains the sn\_mcp\_client.viewer role, a role inheritance on plugin activation.

</td></tr></tbody>
</table>## MCP Client system properties

The following system properties are installed with the Model Context Protocol Client plugin \[sn\_mcp\_client\].

<table id="table_ghh_vt2_xfc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.enable\_mcp\_tool

</td><td>

Enables access to the MCP Client tool on your ServiceNow instance.Default value: **false**

</td></tr><tr><td>

mcp\_guardian\_check

</td><td>

Detects offensive content on the page, when the display output of the tool is set to true and output transformation strategy is null.Default value: **false**

</td></tr></tbody>
</table>## MCP Client tables

The following tables are installed by default with the installation of the Model Context Protocol Client plugin \[sn\_mcp\_client\].

<table id="table_enw_dqv_vfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MCP Execution Logs \[sn\_mcp\_execution\_logs\]

</td><td>

Lists the request and response, the method, a tool call or list call, that was carried out along with the mapped session.The execution logs table also helps debug and shows if there are any errors.

</td></tr><tr><td>

MCP Client Server Session Mappings\[sn\_mcp\_client\_server\_session\_mapping\]

</td><td>

Lists the sessions mapped to the server based on the capabilities support.

</td></tr><tr><td>

Model Context Protocol Servers \[sn\_mcp\_server\]

</td><td>

Lists the MCP servers.

</td></tr></tbody>
</table>