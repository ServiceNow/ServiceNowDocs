---
title: Additional incident context AI agent
description: This AI agent retrieves information beyond the incident itself and presents the output in a readable format. This agent is strictly read-only; it can only retrieve and present information. It cannot update, modify, or perform any write operations on any records \(such as adding comments, changing fields, reassigning, resolving, or closing incidents\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-additional-incident-context-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Additional incident context AI agent

This AI agent retrieves information beyond the incident itself and presents the output in a readable format. This agent is strictly read-only; it can only retrieve and present information. It cannot update, modify, or perform any write operations on any records \(such as adding comments, changing fields, reassigning, resolving, or closing incidents\).

## Workflow

The agent retrieves information such as the caller's hardware assets, the caller's recent incidents, similar resolved incidents, and on-call experts.

1.  Analyze user request and understand intent.
2.  Fetch relevant configuration and data.
3.  Guide user through necessary steps or actions.
4.  Complete the requested operation.
5.  Provide confirmation and next steps.

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

Get callers hardware assets

Get callers recent incidents

Get on call experts

Get similar resolved incidents


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

itil

</td></tr><tr><td>

Data access roles

</td><td>

itil

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

Incident assist

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

