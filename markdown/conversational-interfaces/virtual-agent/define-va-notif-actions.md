---
title: Define Virtual Agent notification actions
description: Create the actions for a Virtual Agent chat or messaging channel to send actionable notifications.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Virtual Agent notifications, Configure, Virtual Agent, Conversational Interfaces]
---

# Define Virtual Agent notification actions

Create the actions for a Virtual Agent chat or messaging channel to send actionable notifications.

## Before you begin

-   An action requires an associated, published \(active\) Virtual Agent topic, a Scriptable action, or a Flow action which can perform the action represented by a button in the notification, such as talk to an agent \(live agent support\) or bot feedback \(Virtual Agent feedback\). Consider working with your topic authors to determine the appropriate topics and corresponding actions. For more information about designing the Virtual Agent topics, see [Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

    **Note:** Scriptable actions and Flow actions are asynchronous and are executed when you select the action without a Virtual Agent topic. You can select either an existing flow that is defined or coordinate with the flow authors to send actionable notifications.

-   Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications** and select the notification for which you are defining actions.

2.  Navigate to the **Notification Actions** related list and select **New Provider Action**.

3.  Select a notification action.

    ![The Notification Action page displaying the notification action types that user can choose and create. The available options are Scriptable Action, Flow Actions, and Virtual Agent.](../images/va-notif-actions-prompt.png "Select notification action")

4.  On the form, fill in the fields to define the notification actions.

<table id="table_gft_nvp_2jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification action. For example, Talk to an agent.

</td></tr><tr><td>

Notification

</td><td>

Notification that is associated with the action. This field is populated automatically with the notification that you created.

</td></tr><tr><td>

Async

</td><td>

Option to enable the action execution without blocking the current request.Both Script and Flow actions in Virtual Agent are asynchronous.

</td></tr><tr><td>

Model Type

</td><td>

Type of actions that are configured. For example, NLU/Keyword topic or LLM topic. If a user selects LLM, that action will be sent to an LLM Virtual Agent. If NLU is selected, that action will only be for an NLU enabled Virtual Agent.

</td></tr><tr><td>

Topic

</td><td>

Virtual Agent topic that handles this notification action.**Note:** Virtual Agent Pro is required to send a topic with actionable notification.

</td></tr><tr><td>

Script

</td><td>

Script to execute the notification action.The script filed is available only when you select Scriptable notification action.

 **Note:** The Scriptable Action is available only for Virtual Agent Pro users.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification content.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification content.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Choose Flow or Action

</td></tr><tr><td>

Flow

</td><td>

Flow to trigger the sequence of the notification action. **Note:**

-   You cannot choose the flow if you provided the action.
-   The Flow field appears only when you select Flow notification action.
-   The Flow Action is available only for Virtual Agent Pro users.


</td></tr><tr><td>

Action

</td><td>

Action to use the correct table and field configuration for the notification action.**Note:**

-   You cannot choose the action if you provided the Flow.
-   The Action field appears only when you select the Flow notification action.
-   The Flow Action is available only for Virtual Agent Pro users.


</td></tr><tr><td class="sub-head" colspan="2">

Inputs

</td></tr><tr><td>

Script

</td><td>

Script to pass inputs to a flow action.This Script field appears when you select the Flow notification action.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  To define another action for the notification, repeat steps 3 through 5.


## What to do next

[Define link actions to notification content](define-va-notif-link-actions.md).

**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)

