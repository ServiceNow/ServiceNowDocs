---
title: Create incident AI agent
description: This AI agent manages the end-to-end process of formally logging IT support requests, specifically for user requests like "create an incident," "raise an incident," "open a new incident," "open an IT ticket," or "raise an IT support ticket."
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-create-incident-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Create incident AI agent

This AI agent manages the end-to-end process of formally logging IT support requests, specifically for user requests like "create an incident," "raise an incident," "open a new incident," "open an IT ticket," or "raise an IT support ticket."

## Workflow

This agent first attempts to resolve the problem with self-service solutions. If the problem persists, it will then intelligently draft a structured IT support incident, confirm the details with the user for accuracy, and create the official record for tracking.

1.  Greet the user and gather information about the issue.
2.  Validate and clarify the user's issue.
3.  Based on the details gathered, create a search query.
4.  Use the search query from as input for the Show Self-Service Options tool. This conversational tool handles the entire self-service process.
5.  Evaluate the outcome. If the issue is solved, workflow is complete. If not, create a new incident with the conversation history.
6.  Confirm the details with the user.
7.  Conclude the conversation based on the outcome.

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

-   **Conversational Topics**

Create Incident Record

Handle Similar Incidents

Show Self-Service Options


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

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

Default VA Workflow

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

