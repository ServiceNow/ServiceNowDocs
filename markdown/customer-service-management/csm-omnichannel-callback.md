---
title: Using Omnichannel Callback for Customer Service Management
description: The ServiceNow Omnichannel Callback for Customer Service Management app enables a callback option for customers when there's a long wait time for a live agent.Additionally, agents can schedule callbacks on behalf of customers from CSM Configurable Workspace
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer communication, Use, Customer Service Management]
---

# Using Omnichannel Callback for Customer Service Management

The ServiceNow® Omnichannel Callback for Customer Service Management app enables a callback option for customers when there's a long wait time for a live agent.Additionally, agents can schedule callbacks on behalf of customers from CSM Configurable Workspace

For more information, see [Omnichannel Callback](https://www.servicenow.com/docs/access?context=omnichannel-callback&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Callback flow

The callback workflow proceeds as follows:

1.  Customers are presented with an option to request a callback when the estimated wait time to reach an agent is too long or when agents are unavailable.
2.  The customer enters callback details such as name, contact details, and the reason for the callback.
3.  Customers request a callback as soon as possible or at a specified date and time.
4.  A callback interaction is created immediately for an immediate callback request or a minute before the selected time for a scheduled callback request.
5.  The ServiceNow® Advanced Work Assignment \(AWA\) application determines the availability of agents and creates a callback work item for an available agent. AWA adds the callback task to the callback queue. The agent then receives a Callback notification in the workspace inbox.
6.  The agent can choose to review the callback context such as knowledge base article views, searches, and Virtual Agent conversation before calling the customer.
7.  The agent calls the customer.
    -   If the customer accepts the call, the interaction is marked as complete when the call ends.
    -   If the customer doesn't accept the call, the agent can retry the callback later.
8.  The agent can decide to close the interaction or queue the callback again manually from the workspace.

![Callback flow diagram](../image/callback-flow-diagram.png "Callback flow diagram")

## Callback requests

-   **Immediate callback request**

    Customers can request a callback immediately. The customers are shown the average time that the agent takes to call back. This request helps to prevent them from having to wait in the queue to connect with an agent.

-   **Scheduling a callback request**

    Customers can request a callback by selecting the preferred date and time. The customer will receive a confirmation of the scheduled callback request via email.

-   **Rescheduling a callback request**

    Customers can reschedule the callback request by choosing from a list of upcoming dates and times for callback requests.

-   **Cancelling a callback request**

    Customers can cancel scheduled callbacks from the self-service channel they requested the callback from.


## Agent-scheduled callbacks

In addition to customer-scheduled callbacks, agents can now create callbacks on behalf of customers from CSM Configurable Workspace. Agent-scheduled callbacks can be created from any omnichannel interaction \(chat, voice, email, messaging\) or case records. Agents can schedule, reschedule, and cancel callbacks.

The following diagram shows the agent-scheduled callback workflow.

![](../image/agent-scheduled-callback-workflow.png "Agent-scheduled callback flow")

-   **Agent-scheduled callback workflow**

    The agent-scheduled callback workflow proceeds as follows:

    1.  Callback creation: While working on a case or during an active interaction, the agent selects Schedule Callback. In the scheduling widget, the agent enters the customer's callback number, preferred date and time, reason for the call, and a short description. The widget displays the customer's time zone. The agent selects **Schedule**.
    2.  Callback task created: The system creates a callback task and links it to the related case or interaction. The callback task state is set to Open.
    3.  Callback confirmation: A confirmation message is displayed indicating that the callback has been scheduled for the customer at the specified time. The message includes a link to the callback record.
    4.  Viewing and managing: Agents can view active callbacks from the Scheduled Callbacks list view and as tiles in the contextual side panel. From either view, agents can reschedule or cancel callbacks for the contact or consumer.

## Callback channels

Customers can request a callback during a chat on Virtual Agent or Engagement Messenger, or from Customer Service Portal. They can request either a phone callback or a video callback on Zoom. Video callbacks must be scheduled but phone callbacks can be requested immediately or scheduled.

**Related topics**  


[Working with callback requests from customers](request-callback-from-agent.md)

[Callback requests by agents](callback-requests-agents-customer.md)

