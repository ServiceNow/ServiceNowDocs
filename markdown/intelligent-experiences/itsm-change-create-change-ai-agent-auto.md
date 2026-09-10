---
title: Create change request AI agent \(autonomous\)
description: This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-change-create-change-ai-agent-auto.html
release: australia
topic_type: reference
last_updated: "2026-09-01"
reading_time_minutes: 3
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI assets, Enable AI experiences]
---

# Create change request AI agent \(autonomous\)

This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.

## Workflow

1.  Initiate the workflow when the user selects the **Create with otto** action from the change request list.
2.  Request the user to describe the change in a single message, including all available details such as affected configuration items, proposed schedule, implementation details, and so on.
3.  Autonomously draft the change request from the user-provided description without requesting additional confirmation or follow-up information.
4.  Delegate to the change template and model suggestion child agent \(Change template suggestion agent\) to autonomously select the best-fit change template and model from the available inventory.
5.  If no template matches with sufficient confidence, apply semantic search over past change requests from the user's assignment group. Identify the most relevant template based on frequency and relevance.
6.  Provide a summary of the change request proposed with fields automatically populated from the user's input and selected template.
7.  User reviews the proposed change request details and either provides additional information or tells the agent to proceed.
8.  Create the change\_request record and return the created change request record number with a link to the record.

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

When enabled, AI specialists can use this agent. This value is off \(true\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Resolve Primary CI before Change creation

Resolve Assignment Group before Change creation

Get change request columns

Get Place holder fields and values from change templates

Create new change request

Set worknote on Change request

-   **Sub-agents**

Change template suggestion agent \(child agent hand-off\)


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

