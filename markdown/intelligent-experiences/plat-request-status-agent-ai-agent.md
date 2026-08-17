---
title: Request status AI agent
description: This AI agent answers inquiries about existing tickets that were created by or are currently opened by the logged-in user. It should be triggered only when the user explicitly references an existing ticket \(for example, by asking for ticket status, updates, comments, or history\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-request-status-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Request status AI agent

This AI agent answers inquiries about existing tickets that were created by or are currently opened by the logged-in user. It should be triggered only when the user explicitly references an existing ticket \(for example, by asking for ticket status, updates, comments, or history\).

## Workflow

The agent handles only tickets, incidents, tasks, or requests that were created or opened by the currently logged-in user. It does not access or manage items submitted by others. The agent doesn't create new requests.

1.  Retrieve the list of tickets that were created or opened by the currently logged-in user.
2.  Display ticket details, status, and available actions:
    -   Add a comment to the ticket
    -   Execute a ticket action
    -   Add an attachment to the ticket
3.  Perform the action and display confirmation to the user.

For more information, see [Platform Request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ticket-status-aia.md).

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

-   **Conversational topic**

Add attachment to the ticket

-   **Scripts**

Add comment to ticket

Execute action

Get actions for ticket

Get last update or details on ticket

Get list of tickets


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

nobody

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
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

