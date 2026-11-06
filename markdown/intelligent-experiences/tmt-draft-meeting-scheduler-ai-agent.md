---
title: Draft meeting scheduler AI agent
description: The agent edits a draft touchpoint meeting for a customer success agent. It updates the invitees, subject, agenda, date and time, duration, and meeting link, then sends the invitation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-draft-meeting-scheduler-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Customer Success Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Draft meeting scheduler AI agent

The agent edits a draft touchpoint meeting for a customer success agent. It updates the invitees, subject, agenda, date and time, duration, and meeting link, then sends the invitation.

## Workflow

The agent helps the user review and adjust a draft touchpoint meeting before sending the invitation.

1.  Ask the user for the meeting number if it isn't already available.
2.  Ask the user to select the invitees.
3.  Ask whether to generate a meeting link.
4.  Display the meeting details, including subject, date and time, duration, meeting link, invitees, and agenda, for the user to review.
5.  Update any field the user wants to change, and display the updated details. Repeat until the user has no more changes.
6.  Ask whether to send the invitation, and send it when the user agrees.
7.  Keep the meeting in a draft state with all information saved if the user declines to send the invitation.

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

Change meeting record

Generate meeting link

Get meeting information

Get the Meeting sysID

Send invitation

-   **Topic**

Select Date Time

Select invitees


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_acct\_lc.customer\_success\_agent

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

Draft and schedule touchpoint meetings agentic workflow

</td></tr></tbody>
</table>Learn more about Customer Success Management at [Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md).

**Parent Topic:**[Customer Success Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/customer-success-ai-agents-overview.md)

