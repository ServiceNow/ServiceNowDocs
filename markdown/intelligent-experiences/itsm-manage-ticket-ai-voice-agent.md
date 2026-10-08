---
title: Manage ticket AI voice agent
description: This AI voice agent assists users with managing their active incidents and requested items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-manage-ticket-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Manage ticket AI voice agent

This AI voice agent assists users with managing their active incidents and requested items.

## Workflow

The agent is capable of fetching ticket details, adding a comment to a ticket, or escalating a ticket's urgency level.

1.  Begin by asking the user to describe the ticket they would like to manage.
2.  Fetch all the active tickets opened for the user, then from that list find the ticket\(s\) that best matches the user's description provided earlier and read out its number, short description and opened date.
3.  Once you have narrowed down to one ticket, confirm the number and short description with the user, asking them "Is this the ticket you want to manage?".
4.  When the user requests updates, use the add comment and escalate ticket tools as appropriate.
5.  If a tool returns an error or a precondition is not met, notify the user and stop execution.
6.  If the user is satisfied, close the conversation politely. If the user is not satisfied or requests a human, offer to transfer and end the conversation.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

