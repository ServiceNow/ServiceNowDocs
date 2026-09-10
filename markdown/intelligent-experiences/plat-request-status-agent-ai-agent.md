---
title: Request status AI agent
description: This AI agent answers inquiries about existing tickets that were created by or are currently opened by the logged-in user. It should be triggered only when the user explicitly references an existing ticket \(for example, by asking for ticket status, updates, comments, or history\).This AI agent enables you to view your open tickets, check the status of tickets, and add comments through ServiceNow Otto for Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-request-status-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 5
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
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

For more information, see [Using the request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-request-status-agent-ai-agent.md).

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

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

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

## Using the request status AI agent

This AI agent enables you to view your open tickets, check the status of tickets, and add comments through ServiceNow Otto for Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.

When you ask for the details of a request, you can perform any other ticket tasks configured by your administrator in the Standard Ticket configuration, such as reopening an incident, and resolving a ticket. You don't need to navigate to a specific page to view your tickets. The AI agent can ask follow-up questions and offer context-aware responses to simplify your experience.

You can upload a file as an attachment to an open ticket or incident to support a request action. For example, if you lose your identity card you may request a replacement using the request status AI agent. You may be asked to upload an email or document that has your manager's approval to get the replacement ID card. In the conversation, you just type, I need to attach a document to this incident or ticket. The AI agent then provides the **Click here to upload a file** option within the AI agent chat for you to upload an attachment to the ticket. You upload the manager approval and the service agent can then approve your request for a new ID.

The tools and triggers that are associated with the request status AI agent are provided by ServiceNow Otto applications. You can activate the AI agent by making triggers active and setting the display settings to include Virtual Agent. If you want to change this AI agent's instructions, you must [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md), adjust the settings to suit your specific needs, and activate the duplicated version of the AI agent instead.

### Prerequisites and setup

To use this AI agent, you must have the Requester Agents - Foundation plugin installed on your instance, which is installed with any other ServiceNow Otto application, such as ServiceNow Otto for IT Service Management \(ITSM\).

To configure which actions are available, a user with the admin or sp\_admin role can configure the Standard Ticket configuration for a table. In the Standard Ticket actions related list, you can add, change, or remove actions. All actions available from the Standard Ticket configuration can be used by the request status AI agent. See [Configure actions for standard ticket page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-actions-for-standard-ticket-page.md) for more information.

To make the AI agent available for users, you must navigate to the **Toggle display** step of the guided setup in AI Agent Studio. Toggle Virtual Agent to `true` and select an assistant.

To make the AI agent available in Microsoft Teams, you must configure an assistant for ServiceNow Otto for Virtual Agent to use a Teams channel. See [Display your assistant on a portal or channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md) for steps to enable Teams for your assistant. Then, in the request status AI agent guided setup in AI Agent Studio, select the assistant you configured for Microsoft Teams in the **Toggle display** step.

### Testing the request status AI agent

You can test the request status AI agent on the Testing page of AI Agent Studio if you have the sn.aia\_admin role. Select the AI agent and use prompts in the **Task** field.

### Sample prompts

After the agent has been activated in AI Agent Studio, enter phrases such as the following or similar queries to run the AI agent in Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.

-   Can you list all open tickets I've created?
-   What's the current status of my incident INC001?
-   Add comment to INC001 "I need your help in fixing this request ASAP. Please prioritize this."
-   Can you check the latest progress on my most recent request?
-   When did I submit this ticket?
-   Who is working on it?
-   I want to add a comment to my ticket.
-   I also want to add an attachment to my ticket.

