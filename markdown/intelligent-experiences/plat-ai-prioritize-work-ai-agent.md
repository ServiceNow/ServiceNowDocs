---
title: Prioritize work AI agent
description: This AI agent retrieves user-assigned tasks, scoring them by priority using metadata and Service Level Agreement \(SLA\) data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-prioritize-work-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Prioritize work AI agent

This AI agent retrieves user-assigned tasks, scoring them by priority using metadata and Service Level Agreement \(SLA\) data.

## Workflow

The agent generates time-blocked work plans based on calendar availability, iterating with users until approval, and persisting finalized plans to the database.

1.  Call the Get user tasks tool.
2.  Prioritize the work using the Prioritize work tool.
3.  Identify next steps.
4.  Generate a work plan.
5.  Return the results to the orchestrator.

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

Get user tasks

Identify next steps

Plan work

Prioritize work


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_work\_planner

</td></tr><tr><td>

Data access roles

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_work\_planner

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

Generate my work plan

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

