---
title: Configure messaging actions
description: Create or modify messaging actions that are performed when an event occurs. These actions apply only to messaging.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure messaging actions

Create or modify messaging actions that are performed when an event occurs. These actions apply only to messaging.

## Before you begin

Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For information on activating this plugin, see [Activate Messaging Actions](activate-messaging-actions.md).

Role required: admin

## About this task

-   For the Requester Message without Agent Response event, the default length of time that elapses before an agent is sent a reminder is 30 minutes.
-   For the Agent Message without Requester Response event, the default length of time that elapses before the conversation is set to the Closed Abandoned state is 2 days.

    If you're using both Virtual Agent and Live Agent, the system closes an abandoned live conversation based on the lowest timeout value for closing conversations. Be aware that other conversation timeout behavior can affect idle live chat timeouts, regardless of the **Duration** and **Action** that you specify. For details, see [Closing Virtual Agent and Agent Chat conversations](https://www.servicenow.com/docs/access?context=va-open-conversations&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).


## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Messaging** &gt; **Actions**.

    -   To create a new messaging action, click **New**.
    -   To update an existing messaging action, click the messaging action.
2.  On the form, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the messaging action.

</td></tr><tr><td>

Event

</td><td>

Event that starts the timer:-   Requester Message without Agent Response - message from a requester that has not been responded to by an agent.
-   Agent Message without Requester Response - message from an agent that has not been responded to by a requester.


</td></tr><tr><td>

Duration

</td><td>

Length of time that elapses after the event before the action runs.

</td></tr><tr><td>

Active

</td><td>

Option to track the timers and perform actions.

</td></tr><tr><td>

Filter Conditions

</td><td>

Condition the timer is evaluated for.

</td></tr><tr><td>

Action

</td><td>

Action to perform after the duration of time has elapsed: -   Prompt Agent - prompt the agent using a Workspace notification.
-   Prompt Requester - display system message with prompt to requester.
-   Reassign - clear the **Assigned to** field of the interaction so that it can be rerouted to another agent.
-   Set State - set the interaction to the given state.


</td></tr><tr><td>

Prompt

</td><td>

Message displayed to requester. This field appears when you select **Prompt Agent** in the **Action** field.

</td></tr><tr><td>

State

</td><td>

State of the interaction. This field appears when you select **State** in the **Action** field.

</td></tr></tbody>
</table>3.  Click **Submit** for a new messaging action or **Update** to modify an existing messaging action.


**Parent Topic:**[Configuring Advanced Work Assignment](../../advanced-work-assignment/task/installing-awa.md)

**Related topics**  


[Advanced Work Assignment home page](../../advanced-work-assignment/concept/awa-admin-console-home.md)

[Get started with Advanced Work Assignment](../../advanced-work-assignment/task/implement-awa.md)

[Install Conversational SMS service channel](../../advanced-work-assignment/task/install-conversational-sms.md)

[Activate Agent Affinity](../../advanced-work-assignment/task/awa-activate-agent-affinity.md)

[Activate Conversational Messaging](activate-messaging-actions.md)

[Service channels](../../advanced-work-assignment/concept/awa-service-channels.md)

[Work items](../../advanced-work-assignment/concept/awa-work-items.md)

[Work assignments](../../advanced-work-assignment/concept/awa-assignment.md)

[Using Agent Affinity](../../advanced-work-assignment/concept/awa-agent-affinity-concept.md)

[Agent Inbox controls](../../advanced-work-assignment/concept/agent-experience.md)

[Advanced Work Assignment Inbox Sentiment display](../../advanced-work-assignment/concept/awa-inbox-sentiment-display.md)

[Management](../../advanced-work-assignment/concept/management.md)

[AWA group queue priorities](../../advanced-work-assignment/concept/awa-group-queue-priorities.md)

[Enable logging for Advanced Work Assignment](../../advanced-work-assignment/task/awa-activate-logging.md)

