---
title: Platform Request status AI agent
description: The Request status AI agent is an AI agent that enables you to view tickets and make updates to them from ServiceNow Otto in Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ticket-status-aia.html
release: zurich
topic_type: concept
last_updated: "2025-11-05"
reading_time_minutes: 4
breadcrumb: [Platform AI agents, AI assets, Enable AI experiences]
---

# Platform Request status AI agent

The Request status AI agent is an AI agent that enables you to view tickets and make updates to them from ServiceNow Otto® in Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.

## Request status AI agent

The Request status AI agent enables you to view your open tickets, check the status of tickets, view a summary of the previous comments from the AI agent or others working on the ticket, and add comments through ServiceNow Otto in Virtual Agent, the ServiceNow Otto panel, or Microsoft Teams.

You can upload a file as an attachment to an open ticket or incident to support a request action. For example, if you lose your identity card you may request a replacement in the Request status AI agent. You may be asked to upload an email or document that has your manager's approval to get the replacement ID card. In the Request status AI agent, you just type, I need to attach a document to this incident or ticket. The Request status AI agent then provides the **Click here to upload a file** option within the AI agent chat for you to upload an attachment to the ticket. You upload the manager approval and the service agent can then approve your request for a new ID.

To find more information about an open ticket, you can ask the Request status AI agent follow-up questions based on previous answers from the agent. For example:

-   Can you check the latest progress on my most recent request?
-   When did I submit this ticket?
-   Who is working on it?
-   I want to add a comment to my ticket.
-   I also want to add an attachment to my ticket.

When you ask for the details of a request, you can perform any other ticket tasks configured by your administrator in the Standard Ticket configuration. For example, reopening an incident and resolving a ticket. You don't need to navigate to a specific page to view your tickets. The AI agent can ask follow-up questions and offer context-aware responses to simplify your experience.

The tools and triggers associated with the Request status AI agent are provided by ServiceNow Otto applications. You can activate the AI agent by making triggers active and setting the display settings to include Virtual Agent. If you want to change this AI agent's instructions, you must [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/clone-ai-agent.md), adjust the settings to suit your specific needs, and activate the duplicated version of the AI agent instead.

## Prerequisites and setup

This AI agent is installed with certain applications. Check your entitlements for details.

To configure which actions are available, a user with the admin or sp\_admin role can configure the Standard Ticket configuration for a table. In the Standard Ticket actions related list, you can add, change, or remove actions. All actions available from the Standard Ticket configuration can be used by the Request status AI agent. See [Configure actions for standard ticket page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-actions-for-standard-ticket-page.md) for more information.

To make the Request status agent available for users, you must navigate to the **Toggle display** step of the guided setup in AI Agent Studio. Toggle Virtual Agent to `true` and select an assistant.

To make the Request status AI agent available in Microsoft Teams, you must configure an assistant for ServiceNow Otto in Virtual Agent to use a Teams channel. See [Display your assistant on a portal or channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/display-assistant-portal-channel.md) for steps to enable Teams for your assistant. Then, in the Request status AI agent guided setup in AI Agent Studio, select the assistant you configured for Microsoft Teams in the **Toggle display** step.

## Role masking

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/define-sec-controls-aia.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to evaluate for readiness. For example, you can add the itil role to the AI agent's list of approved roles so that it can access Incident records.

## Accessing the Request status AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select **Request status AI agent**.

## Testing the Request Status AI agent

You can test the Request Status AI agent on the Testing page of AI Agent Studio if you have the sn.aia\_admin role. Select the AI agent and use utterances in the **Task** field like the following examples:

## Sample utterances

After the agent has been activated in AI Agent Studio, enter phrases such as the following or similar queries to run the AI Agent in Virtual Agent, the Now Assist panel, or Microsoft Teams.

-   Can you list all open tickets I've created?
-   What's the current status of my incident INC001?
-   Add comment to INC001 "I need your help in fixing this request ASAP. Please prioritize this."
-   Can you check the latest progress on my most recent request?

**Parent Topic:**[Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/platform-ai-agents.md)

