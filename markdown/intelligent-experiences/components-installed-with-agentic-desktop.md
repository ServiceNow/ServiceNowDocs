---
title: Components installed with Agentic Desktop
description: Several types of components are installed with activation of the sn\_desktop\_agents plugin, including user roles and tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Reference, Agentic Desktop, Enable AI experiences]
---

# Components installed with Agentic Desktop

Several types of components are installed with activation of the sn\_desktop\_agents plugin, including user roles and tables.

## Roles installed

<table id="table_y3j_1x3_hhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI Agent Admin \[sn\_aia.admin\]

</td><td>

Enables you to create, manage, and test desktop actions in Agentic Desktop and deploy them as tools in AI Agent Studio.

</td><td>

-   agent\_role\_config\_admin
-   sn\_skill\_builder.admin
-   connection\_admin
-   flow\_designer
-   sn\_aia.viewer
-   sn\_mcp\_client.admin
-   sn\_ace.ace\_user

</td></tr><tr><td>

Now Assist panel user \[now\_assist\_panel\_user\]

</td><td>

Enables you to trigger desktop actions from Now Assist panel and execute desktop actions in the desktop environment using Execution workspace.

</td><td>

sn\_nowassist\_admin.user

</td></tr></tbody>
</table>## Tables installed

<table id="table_cjj_1x3_hhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Desktop action\[sn\_desktop\_core\_action\]

</td><td>

Stores details, such as input and output parameters and number of screens for desktop actions of type UI block.

</td></tr><tr><td>

Desktop action application\[sn\_desktop\_core\_action\_application\]

</td><td>

Stores the desktop application associated with the desktop action.

</td></tr><tr><td>

Desktop action execution \[sn\_desktop\_core\_action\_execution\]

</td><td>

Stores the execution details of a desktop action, such as request, response, tool execution, and execution plan.

</td></tr><tr><td>

Desktop action parameter\[sn\_desktop\_core\_action\_parameter\]

</td><td>

Stores the desktop action parameter records as parent records.

</td></tr><tr><td>

Desktop action parameter value\[sn\_desktop\_core\_action\_parameter\_value\]

</td><td>

Stores the desktop action parameter value records as child records.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_xq5_tgy_whc"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agentic Desktop\[com.sn\_desktop\_agents\]

</td><td>

Contains configuration of desktop action tool used by AI Agent Studio to discover available desktop actions while creating AI agents and invoke desktop actions via AI agents during execution.

</td></tr><tr><td>

Agentic Desktop Core\[com.sn\_desktop\_core\]

</td><td>

Packages tables, custom functionality specific to Agentic Desktop application, and Agentic Desktop download interface within a scoped application.

</td></tr></tbody>
</table>**Parent Topic:**[Agentic Desktop reference](agentic-desktop-reference.md)

