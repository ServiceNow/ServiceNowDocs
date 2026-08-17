---
title: OT knowledge generator AI agent
description: This AI agent creates a KB Article from a resolved Operational Technology incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/otsm-ot-knowledge-generator-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Operational Technology Service Management AI agents, Operational Technology Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# OT knowledge generator AI agent

This AI agent creates a KB Article from a resolved Operational Technology incident.

## Workflow

1.  Inform user that the KB article generation process has begun.
2.  If the user has provided the sys\_id of the incident, use the OT Knowledge generator tool to generate a KB article.
3.  End the conversation regardless of the results.

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

-   **Subflow**

OT Knowledge generator


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ot\_incident\_write

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ot\_incident\_write

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

Generating a KB article upon resolving an OT Incident

</td></tr></tbody>
</table>Learn more about Operational Technology at [Operational Technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-overview.md).

**Parent Topic:**[Operational Technology Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/otsm-ai-agents-overview.md)

