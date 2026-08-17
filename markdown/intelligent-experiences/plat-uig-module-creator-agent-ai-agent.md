---
title: Module creator AI agent
description: This ServiceNow Otto for Creator agent Converts natural language requests into structured JSON definitions for ServiceNow application navigator modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-uig-module-creator-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Module creator AI agent

This ServiceNow Otto for Creator agent Converts natural language requests into structured JSON definitions for ServiceNow application navigator modules.

## Workflow

1.  Parse the user's request to identify one or more modules to create, including module type, table, view, role, filter criteria, and other properties.
2.  Determine whether each module is a modern \(Next Experience\) or legacy \(Core UI\) type based on keywords in the request.
3.  Look up tables, views, roles, assessments, reports, map pages, or timeline pages as needed, but only when the user explicitly references a specific record by name. If not specified, output minimal JSON.
4.  Convert any filter conditions to encoded query format using the Encoded Query Generator tool.
5.  Generate a context-aware title for each module based on the table, filter, or user-specified name.
6.  Output the final JSON array and call the Process Output tool.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Assessment Lookup

Encoded Query Generator

Map Pages Lookup

Process Output

Reports Lookup

Role Lookup

Table Lookup

Timeline Pages Lookup

View Lookup


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Creator at [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator-landing.md).

**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

