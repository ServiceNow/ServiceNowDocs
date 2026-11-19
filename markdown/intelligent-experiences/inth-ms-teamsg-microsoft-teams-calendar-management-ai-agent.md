---
title: Microsoft Teams calendar management AI agent
description: This AI agent manages Microsoft Teams meetings. It looks up meeting details and the occurrences of a recurring meeting, and deletes meetings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-ms-teamsg-microsoft-teams-calendar-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Microsoft Teams Graph Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Microsoft Teams calendar management AI agent

This AI agent manages Microsoft Teams meetings. It looks up meeting details and the occurrences of a recurring meeting, and deletes meetings.

## Workflow

The agent helps the user review and remove Microsoft Teams meetings.

1.  Ask the user what they want to do and collect the details the action needs, such as the meeting ID or organizer.
2.  Look up a meeting's details.
3.  Look up the occurrences of a recurring meeting.
4.  Delete a meeting.
5.  Report the outcome to the user, including details of any error.

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

-   **Flow Actions**

Delete meeting

Look up meeting

Look up meeting occurrences


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Teams Graph Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-ms-teamsg-ai-agents-overview.md)

**Related topics**  


[Microsoft Teams Graph Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/msteams-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md)

