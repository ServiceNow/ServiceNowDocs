---
title: Using Omnichannel Callback for Customer Service Management
description: The ServiceNow Omnichannel Callback for Customer Service Management app enables a callback option for customers when there’s a long wait time for a live agent.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customer communication, Using Customer Service Management, Customer Service Management]
---

# Using Omnichannel Callback for Customer Service Management

The ServiceNow® Omnichannel Callback for Customer Service Management app enables a callback option for customers when there’s a long wait time for a live agent.

For more information, see [Omnichannel Callback](https://www.servicenow.com/docs/access?context=omnichannel-callback&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

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
    -   If the customer doesn’t accept the call, the agent can retry the callback later.
8.  The agent can decide to close the interaction or queue the callback again manually from the workspace.

![Callback flow diagram](../image/Omni-callback-flow.png "Callback flow diagram")

## Callback requests

-   **Immediate callback request**

    Customers can request a callback immediately. The customers are shown the average time that the agent will take to call back. This request prevents them from having to wait in the queue to connect with an agent.

-   **Scheduling a callback request**

    Customers can request a callback by selecting the preferred date and time. The customer will receive a confirmation of the scheduled callback request via email.

-   **Rescheduling a callback request**

    Customers can reschedule the callback request by choosing from a list of upcoming dates and times for callback requests.

-   **Cancelling a callback request**

    Customers can cancel scheduled callbacks from the self-service channel they requested the callback from.


## Callback channels

Customers can request a callback during a chat on Virtual Agent or Engagement Messenger, or from Customer Service Portal. They can request either a phone callback or a video callback on Zoom. Video callbacks must be scheduled but phone callbacks can be requested immediately or scheduled.

