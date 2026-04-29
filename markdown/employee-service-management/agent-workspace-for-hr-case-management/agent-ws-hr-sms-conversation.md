---
title: SMS conversations in HR Service Delivery Agent Workspace
description: Using the Conversational SMS service channel app, available on the ServiceNow Store, HR agents can provide support for long-running SMS conversations via HR Service Delivery Agent Workspace. Requesters can initiate HR support conversations through SMS.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# SMS conversations in HR Service Delivery Agent Workspace

Using the Conversational SMS service channel app, available on the ServiceNow Store, HR agents can provide support for long-running SMS conversations via HR Service Delivery Agent Workspace. Requesters can initiate HR support conversations through SMS.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## SMS support conversations

SMS support conversations can run long. For this reason, HR Service Delivery workspace agents need the ability to track ongoing conversations on the HR SMS service channel. HR Service Delivery workspace agents can initiate or continue SMS conversations and also accept SMS work items from the HR Service Delivery Agent Workspace Inbox.

For SMS support conversations, in the Workspace Chat panel, when the interaction type is **Messaging**, an interaction sub-type of **SMS** is indicated as **Active SMS**.

For complete details about SMS support conversations, associated service channels, requestor initiated, and agent initiated SMS conversations, refer to [Conversational SMS service channel](https://www.servicenow.com/docs/access?context=conversation-sms-service-channel-store-app&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## SMS support conversations for HR Service Delivery agents

HR agents can access new SMS messaging interactions, as well as access ongoing SMS messaging conversations. Agents can switch from an in-progress messaging interaction, such as a chat, to a new SMS messaging interaction.

Advanced Work Assignment HR agents and managers can end an SMS messaging conversation. HR agents with the awa\_agent role can end an active SMS messaging conversation assigned to them using the **End conversation** action button. Users with the awa\_manager role can end the conversation even when it is not assigned to them on the interaction. When an agent ends the conversation, a confirmation to close the interaction appears.

HR AWA agents and managers can switch from an in-progress messaging interaction to a new messaging conversation. Switching to a new messaging interaction does not close the original messaging interaction, but enables agents to carry on multiple messaging conversations. AWA agents can access ongoing messaging conversations when the HR AWA agents and managers have access to ongoing messaging conversations and are notified when there is a new message on any long running assigned interactions. When an ongoing messaging conversation has a new message that needs attention, an icon is displayed after the Inbox icon in HR Service Delivery Workspace. A new tab carries a counter badge that indicates the number of messaging conversations that have unread messages. AWA agents and managers can view cards for messaging conversations.

HR AWA agents and managers can view a list of all **In Progress** or **On Hold Messaging Work Items** assigned to other agents. The list indicates the service channel, interaction number, and last updated date. Agents can click the list item to open it in a Workspace tab. Agents can open a messaging interaction in a sub tab and, if the interaction is active, view the chat panel on the interaction record. Agents can type messages in the chat panel to have an SMS conversation with an employee.

## Quick actions for agents

Access existing chat-based quick actions for SMS messaging. For details, refer to [Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-exploring&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Conversation desktop notifications

HR agents can set preferences to receive conversation desktop notifications, audio alerts, and Google Chrome browser toasts. Audio alerts and desktop notifications occur when agents opt in to receiving **Conversation Audio Alerts** and **Conversation Desktop Notifications** via the HR Service Delivery Agent Workspace Inbox settings.

Once opted in, agents hear an audio alert when a new message occurs on a conversation that is currently open in a workspace tab, but not in focus. Audio alerts also notify when a long running conversation is assigned to an agent, but is not currently open in a workspace tab. Agents decide if they want to enable these alerts and notifications.

Use the edit menu ![edit menu icon](../../../common/image/gear.png) in the HR Service Delivery Agent Workspace Inbox to enable alerts and notifications.

![HRSD Agent Workspace Inbox settings](../image/SMS-hr-inbox-notifications-settings.png)

Agents can receive Google Chrome browser toasts when the following criteria is met:

-   The agent has opted in to receive **Conversation Desktop Notifications**.
-   The agent is using Google Chrome browser.
-   The Workspace browser tab is not in focus.
-   A new message on an existing conversation, assigned to the agent, is in one of the following places:
    -   A currently open Workspace tab.
    -   Not in a currently open Workspace tab, but in a long running conversation in an ongoing section of Workspace.

## Employee initiated SMS conversations

Employees can initiate HR support conversations through SMS. Agents can expect the system to automatically associate the sender phone number to the channel user profile. If an SMS message is received for a non-existing channel user profile, a new channel user profile is automatically created by the system. The system queries the **Mobile phone** field on employee HR profile for a match. When a match is found, the system associates the employee with the newly created channel user profile. If more than one match is found no association is made on the channel user profile. If no match is found no association is made on channel user profile.

When an employee adds a phone number to an SMS messaging interaction or updates a phone number on the interaction, the Number field on the interaction updates from null to the employee's name. The HR profile for that employee is associated to the phone number. Only one active channel user profile can exist for a given phone number at any time.

