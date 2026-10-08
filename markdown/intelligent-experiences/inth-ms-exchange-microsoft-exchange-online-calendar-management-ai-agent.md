---
title: Microsoft Exchange Online calendar management AI agent
description: This AI agent manages Microsoft Exchange Online calendars. It creates and deletes events, finds meeting times, manages event attachments, and looks up calendars, events, occurrences, calendar views, and time zones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-ms-exchange-microsoft-exchange-online-calendar-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Exchange Online Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Microsoft Exchange Online calendar management AI agent

This AI agent manages Microsoft Exchange Online calendars. It creates and deletes events, finds meeting times, manages event attachments, and looks up calendars, events, occurrences, calendar views, and time zones.

## Workflow

The agent helps the user manage calendars and events in Microsoft Exchange Online.

1.  Ask the user what they want to do and collect the details the action needs, such as the user, calendar, or event.
2.  Look up calendars, a calendar by ID, or a user's calendar events.
3.  Look up an event by ID, a calendar view, or the occurrences of a recurring series.
4.  Find meeting times and create a calendar event.
5.  Copy an attachment to an event, look up an event's attachments, or delete an attachment.
6.  Delete a calendar event or event record.
7.  Look up available time zones.
8.  Report the outcome to the user, including details of any error.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Copy Attachment to Calendar Event

Delete Attachment

Delete Calendar Event

Look up Attachments by Event ID

Look up Calendar Events by User ID

Look up Calendar View Stream

Look up Calendar by ID

Look up Calendars Stream

Look up Event by ID

Look up Occurrence Stream by SeriesMaster ID

Look up Time Zones

-   **Subflows**

Create Calendar Event

Delete Event Record

Find Meeting Times


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Exchange Online Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-ms-exchange-ai-agents-overview.md)

**Related topics**  


[Microsoft Exchange Online Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/ms-exch-online-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

