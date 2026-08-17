---
title: Incident routing configuration AI agent
description: This AI agent creates, modifies, and deactivates assignment rules for incident routing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-incident-routing-configuration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Incident routing configuration AI agent

This AI agent creates, modifies, and deactivates assignment rules for incident routing.

## Workflow

The agent provides end-to-end support, from rule activation and AI recommendations to manual rule creation and bulk changes, with a staged commit workflow that lets users preview before applying.

1.  Greet and retrieve configuration status.
2.  Display best practices.
3.  Set up business rules if none are active.
4.  Set up assignment rules if none are active.
5.  Review and confirm with the user.
6.  Commit changes.
7.  Gather routing preferences from the user.
8.  Generate and display routing recommendations.
9.  Handle user selection and changes.
10. Preview and commit changes, if approved.

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

-   **Generative AI skill**

Incident Routing Rule Recommender

-   **Scripts**

Payload Manager

Text to encoded query for incident routing agent

-   **Flow action**

Preview tool action


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

admin

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

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

