---
title: Ticket creation AI agent
description: The agent creates a service problem case for a connectivity issue. It checks that the sold product, short description, and experience profile are available, creates the case, and displays the case number with a link to the new record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-ticket-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Ticket creation AI agent

The agent creates a service problem case for a connectivity issue. It checks that the sold product, short description, and experience profile are available, creates the case, and displays the case number with a link to the new record.

## Workflow

The agent creates a service problem case for the user's connectivity issue and gives them a link to it.

1.  Check that the sold product, the short description, and the experience profile are available, and tell the user when the record is missing or invalid.
2.  Tell the user that a service problem case is being created for their connectivity issue.
3.  Create the service problem case with the sold product, short description, and experience profile.
4.  Display the case number and a link to the new case.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Create service problem case


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_sprb\_mgmt.agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Customer voice quality issue resolution

</td></tr></tbody>
</table>Learn more about Customer Service Problem Management at [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cspm-landing-page.md).

**Parent Topic:**[Customer Service Problem Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cspm-ai-agents-overview.md)

