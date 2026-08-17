---
title: Care Team Operations case creation AI agent
description: This AI agent streamlines case creation by analyzing user conversations to accurately determine the service definition for each reported issue. It intelligently identifies multiple issues raised in a single conversation and creates separate cases with correct case type and service definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cto-care-team-operations-case-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Care Team Operations AI agents, Care Team Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Care Team Operations case creation AI agent

This AI agent streamlines case creation by analyzing user conversations to accurately determine the service definition for each reported issue. It intelligently identifies multiple issues raised in a single conversation and creates separate cases with correct case type and service definition.

## Workflow

The agent helps users complete tasks related to care team operations case creation.

1.  From the request summaries generated, note the case type for each distinct request.
2.  Read the service definitions for Care Team Operations applications for each case type identified in Step 1.
3.  Identify the service definition.
4.  Identify the category.
5.  Create care team operations case.

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

-   **Conversational topic**

Create care team cases

-   **Script**

Get service definition details


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_hco.care\_team\_member, sn\_hco.care\_team\_manager

</td></tr><tr><td>

Data access roles

</td><td>

sn\_hco.care\_team\_member, sn\_hco.care\_team\_manager

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

Request care team assistance

</td></tr></tbody>
</table>Learn more about Healthcare Operations at [Healthcare Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-operations-overview.md).

**Parent Topic:**[Care Team Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/care-team-operations-ai-agents-overview.md)

