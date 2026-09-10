---
title: Components installed with AI Desktop Actions
description: Several types of components are installed with activation of the sn\_desktop\_agents plugin, including user roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/components-installed-with-agentic-desktop.html
release: australia
topic_type: reference
last_updated: "2025-11-13"
reading_time_minutes: 4
breadcrumb: [Reference, AI Desktop Actions, Enable AI experiences]
---

# Components installed with AI Desktop Actions

Several types of components are installed with activation of the sn\_desktop\_agents plugin, including user roles and tables.

## Roles used

<table id="table_y3j_1x3_hhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI Agent Admin\[sn\_aia.admin\]

</td><td>

Enables you to create, manage, and test desktop actions in AI Desktop Actions and deploy them as tools in AI Agent Studio.

</td><td>

-   agent\_role\_config\_admin
-   sn\_skill\_builder.admin
-   connection\_admin
-   flow\_designer
-   sn\_aia.viewer
-   sn\_mcp\_client.admin
-   sn\_ace.ace\_user

</td></tr><tr><td>

ServiceNow Otto panel user\[now\_assist\_panel\_user\]

</td><td>

Enables you to trigger desktop actions from ServiceNow Otto panel and execute desktop actions in the desktop environment using Execution workspace.

</td><td>

sn\_nowassist\_admin.user

</td></tr><tr><td>

Desktop action user\[sn\_desktop\_core.desktop\_action\_user\]

</td><td>

Enables you to create desktop actions using the **Record with AI** feature in AI Desktop Actions.

</td><td>

-   sn\_aia.admin
-   sn\_nowassist\_admin.user

</td></tr><tr><td>

Web Agent Runtime\[sn\_naa.web\_agent\_runtime\]

</td><td>

Grants the Web Automation Agent's service account read and write access to data required during execution.Assign this role only to the service account the agent runs as \(not to end users\). Without this role, the agent can't read or write any data at runtime.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_cjj_1x3_hhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Desktop action\[sn\_desktop\_core\_action\]

</td><td>

Stores details, such as input and output parameters and number of screens for on-screen desktop actions.

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

AI Desktop Actions\[com.sn\_desktop\_agents\]

</td><td>

Contains configuration of desktop action tool used by AI Agent Studio to discover available desktop actions while creating AI agents and invoke desktop actions via AI agents during execution.

</td></tr><tr><td>

AI Desktop Actions Core\[com.sn\_desktop\_core\]

</td><td>

Packages tables, custom functionality specific to AI Desktop Actions application, and AI Desktop Actions download interface within a scoped application.

</td></tr><tr><td>

ServiceNow Otto AI web agents\[sn\_naa\]

</td><td>

Contains system properties, default AI agent and agentic workflow named Web Automation Agent and Web Automation respectively, and functionality to perform adaptive automation on web.

</td></tr></tbody>
</table>## System properties installed

<table id="table_hkb_zvg_ljc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_desktop\_core.record\_with\_ai

</td><td>

Makes **Record with AI** the default recording option. Turn off this property to set the manual recorder as the default recording option.-   Type: true \| false
-   Default: true

</td></tr><tr><td>

sn\_desktop\_core.max\_action\_events

</td><td>

Modifies the limit of maximum number of events processed during a single Desktop action execution in AI Desktop Actions.-   Type: Integer
-   Default: 200

</td></tr><tr><td>

sn\_naa.ai\_web\_agent.enabled

</td><td>

Enables or disables the adaptive desktop actions on the instance. Set to 'true' to enable the web agent, or 'false' to disable it.-   Type: true \| false
-   Default: true

Roles and permissions

sys\_admin: Read

</td></tr><tr><td>

sn\_naa.allowed\_websites

</td><td>

Stores a list of websites that AI agents configured with adaptive desktop actions are permitted to open and perform tasks.Type: String

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.context\_closing\_frequency

</td><td>

Specifies, in hours, how long to wait before closing orphaned, running `sn_naa_context` records in the database.-   Type: integer
-   Default: 24

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.keep\_tab\_open

</td><td>

Keeps the browser tabs that open during goal execution open after the goal completes.

 Whenever you update the value, select the **ServiceNow Web Automation** extension icon, and save the instance provided in the extension.

 -   Type: true \| false
-   Default: true

 Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.min\_web\_agent\_version

</td><td>

Specifies the minimum adaptive desktop action \(browser extension\) version required for this instance to function correctly. If the installed version is lower than this value, the system will not run.Type: string

Roles and permissions

sys\_admin: Read

</td></tr><tr><td>

sn\_naa.NaaModeratorToolTimeLimit

</td><td>

Specifies the maximum duration, in milliseconds, that the web automation tool is allowed to run before it's considered a failure.-   Type: integer
-   Default: 1800000

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.reasoning.manual\_intervention\_prompt

</td><td>

Instructs the system to pause and request explicit input, confirmation, or a decision from the user in scenarios that require manual intervention.Type: string

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.step\_record\_cleanup\_frequency

</td><td>

Specifies, in days, how long to wait before permanently deleting `sn_naa_step` records from the database.-   Type: Integer
-   Default: 90

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.web\_agent.compaction\_enabled

</td><td>

Enables summarization of steps that exceed the history limit, rather than discarding them. When turned off, only the most recent configured number of steps are retained.-   Type: true \| false
-   Default: true

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.web\_agent.compaction\_history\_limit

</td><td>

Sets the maximum number of unsummarized steps allowed before the oldest batch is summarized. When unsummarized steps exceed this value, compaction is triggered.-   Type: Integer
-   Default: 15

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.web\_agent.summarization\_batch\_size

</td><td>

Sets the number of steps combined into a single summary. Larger batches reduce how often summarization runs, but produce less granular summaries.-   Type: Integer
-   Default: 10

Roles and permissions

-   sys\_admin: Read and Write
-   sn\_naa\_admin: Read and Write

</td></tr><tr><td>

sn\_naa.web\_agent\_environment\_type

</td><td>

Specifies the adaptive desktop action execution type. Set to `cloud`, which runs execution in the cloud.

Set it to `local` to run execution through the browser extension.

-   Type: choice list
-   Default: cloud

Roles and permissions

sys\_admin: Read

</td></tr></tbody>
</table>**Parent Topic:**[AI Desktop Actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-reference.md)

