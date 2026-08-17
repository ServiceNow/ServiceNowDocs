---
title: Automation table discovery AI agent
description: This Workflow Data Fabric agent collects asset, time, and scope inputs from the user and returns a structured JSON payload identifying the target execution tables for automation discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-ac-automation-table-discovery-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Automation table discovery AI agent

This Workflow Data Fabric agent collects asset, time, and scope inputs from the user and returns a structured JSON payload identifying the target execution tables for automation discovery.

## Workflow

1.  Prompt the user for an automation asset they want to analyze. If the user selects **Other**, switch to an alternate path that collects a free-text description and discovers matching execution tables.
2.  Ask the user what time range to analyze.
3.  Ask which application scope\(s\) to search across.
4.  Display a confirmation message summarizing the selections, then output a structured JSON payload for a downstream workflow to execute the actual search.

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

Discover &amp; Resolve Exec Tables

LoadBaseCtx

Questionnaire


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ac.automation\_technical\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ac.automation\_technical\_user

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Automation Explorer

</td></tr></tbody>
</table>Learn more about Workflow Data Fabric at [Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

**Parent Topic:**[Workflow Data Fabric AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/wdf-ai-agents-overview.md)

