---
title: Meeting scheduler AI agent
description: This AI agent specializes in organizing Zoom or Microsoft Teams meetings and creating regular calendar events with ease. It helps users find available time slots and set up meetings effortlessly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-meeting-scheduler-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Integration Hub AI agents, Integration Hub, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Meeting scheduler AI agent

This AI agent specializes in organizing Zoom or Microsoft Teams meetings and creating regular calendar events with ease. It helps users find available time slots and set up meetings effortlessly.

## Workflow

1.  Determine whether the user has specified a preferred meeting type \(Zoom, Microsoft Teams, or a standard calendar event\).
2.  Fetch the email address of the currently logged-in user.
3.  Identify the title, subject, or purpose of the meeting from the user's request.
4.  Check if any attendees are provided in the request.
5.  Check whether the request includes any date, day, or time reference \(such as Monday, Today, Morning, Tomorrow, 3 PM, 03:00:00, and so on\).
6.  Identify if an email body is provided in the user's request.
7.  Check if any time zone is mentioned in the user's request.
8.  If the user requests to add a room or location for the meeting, ask for room name, city, and minimum capacity.
9.  Find available meeting times.
10. Show the user a preview of the meeting invitation.
11. Create the event if the user approves.

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

-   **Subflows**

Create Calender Event

Find Meeting Times

Generate Zoom Meeting URL

-   **Knowledge Graph**

Fetch attendees from the ServiceNow Users table

-   **Script**

Fetch Logged in User's Timezone and email address

-   **Flow Actions**

Fetch Relevant Users

Look up Rooms


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Integration Hub at [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md).

**Parent Topic:**[Integration Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrationhub-ai-agents-overview.md)

