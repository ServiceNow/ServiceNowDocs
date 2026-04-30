---
title: Configuring Virtual Agent notifications
description: Send ServiceNow notifications directly to users via the Virtual Agent chatbot on supported messaging channels. Notifications can be simple informational messages for review, or actionable messages with buttons that users can select to perform certain actions.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-05-15"
reading_time_minutes: 6
keywords: [Configuring, Virtual Agent, notifications, SMS, Twilio, Messenger, MSTeams, Microsoft Teams]
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configuring Virtual Agent notifications

Send ServiceNow notifications directly to users via the Virtual Agent chatbot on supported messaging channels. Notifications can be simple informational messages for review, or actionable messages with buttons that users can select to perform certain actions.

Notifications are sent to recipients via the Virtual Agent bot in the chat widget, pre-built messaging integrations \(for example, SMS Twilio, Slack, Microsoft Teams, Workplace from Facebook services, and Facebook Messenger messaging platform\), and custom chat integrations.

Notification functionality is included with the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin and also with Virtual Agent Lite, which is included with the ServiceNow AI Platform. However, Virtual Agent Lite users can receive only simple notifications, while Virtual Agent users can receive both actionable notifications and simple notifications. Users with no associated ServiceNow profiles in the \[sys\_user\] table can receive non-actionable Virtual Agent notifications.

## How Virtual Agent notifications work

As an admin, you can define different types of notifications that have specific layouts and content. You can also customize certain aspects of notification content, such as the message heading and message content.

-   **Simple notifications**

    The content can be a standard informational message, record card, or an image card. Simple notifications are delivered to users immediately, even when they're engaged in a conversation with a virtual or live agent.

-   **Actionable notifications**

    These notifications have buttons that enable the recipient to perform certain actions, such as adding a comment or requesting a live agent. When you create an actionable notification, you associate an action with a published Virtual Agent topic, a scriptable action, or a flow action that handles the action to be performed. To encourage users to act on a notification, admin users can choose to remove the **Skip** option. If the user still doesn’t act, the conversation will be completed as inactive.

    **Note:** The notifications are actionable only when there is an associated link action to its content.

    Actionable notifications are delivered to users when they're not in an active conversation with a virtual or live agent. A queue stores actionable notifications that are waiting to be delivered, for up to eight hours by default.

    Actionable notifications are best suited for conversational purposes, such as:

    -   Password reset
    -   Incident update
    -   Approval request
    -   Course survey
    -   Service follow-ups and surveys
    -   Employee onboarding follow-ups
    When a topic conversation completes, Virtual Agent automatically prompts the user to view pending notifications \(if any\). Admins can suppress this prompt by setting the **com.glide.cs.show\_pending\_notifications\_prompt** property on the System Properties table to false.

-   **Notifications with dynamic content**

    You can personalize Virtual Agent notifications by adding dynamic content to message headers and messages. For record- and event-based notifications, you use parameter substitution to specify the variables that identify the record values \(from the notification table\) to be included in the content.

-   **Advanced notifications with dynamic content**

    You can create Virtual Agent notifications that use a script to add dynamic content in message headers and messages. The content can come from multiple data sources and include third-party services, such as URL shortening.

-   **Variables in notifications**

    You can pass information to a completed survey when the notification is triggered. Context is defined by the script found in the notification topic. This script cannot be modified.

    ```
    vaVars.global_notification_context = 
      JSON.stringify({
        'tableName': table_name, 
            'tableSysId': sys_id, 
            'actionId': actionId, 
            'eventParm1': eventParm1, 
            'eventParm2': eventParm2});
    ```

    Notifications are triggered by records updates or by creating a platform event in the event queue. `actionId` is the ID number for the action. The platform event takes in the `eventParm1` and `eventParm2` parameters. If a notification is triggered, the parameters are passed to the topic. To capture the notification incident number in your topic, use the following script.

    ```
    var notificationContext = JSON.parse(vaVars.global_notification_context);
    vaVars.sysId = notificationContext.tableSysId;
    varVars.tableName = notificationContext.tableName;
    ```


## Notification processing

Virtual Agent notifications have certain processing controls and limitations, such as the maximum number of recipients allowed per notification and the number of notifications that can be sent per day. The following table identifies these processing controls and the system properties that can be used to change their default values.

<table id="table_ly5_b15_hsb"><thead><tr><th>

Notification processing control or limitation

</th><th>

Default value

</th><th>

Associated system property

</th></tr></thead><tbody><tr><td>

Maximum number of recipients per notification per channel

</td><td>

100,000 recipients

</td><td>

**com.glide.cs.per\_notification\_user\_limit** Max limit: None

**Note:**

-   If there are more recipients than the configured number, warning messages are displayed to reduce the recipient list while you’re configuring the notification and when the notification is delivered. The warnings are displayed only when there is Virtual Agent content associated with the notification.
-   Recipient limits may apply to third-party delivery channels based on the level of service or subscription.

</td></tr><tr><td>

Maximum number of notifications per day, per channel

</td><td>

100,000 notifications

</td><td>

**com.glide.cs.daily\_notification\_limit**Max limit: None

**Note:** Rate limits may apply to third-party delivery channels based on the level of service or subscription.

</td></tr><tr><td>

Lifespan of actionable notifications \(a queue stores actionable notifications that are waiting to be delivered\)

</td><td>

8 hours

</td><td>

**com.glide.cs.idle\_actionable\_notification\_timer** **Note:** You can specify a maximum value of 72 hours.

</td></tr><tr><td>

Allow access to notification card content and parameter substitutions in notification headings and messages

</td><td>

False \(not enabled\)

</td><td>

**com.glide.cs.notification\_record\_access\_check** **Note:** This property does not apply to advanced notifications.

</td></tr></tbody>
</table>## Notification experience for end users

The notification experience for end users depends on the type of notification that they're receiving. End users can also manage how their notifications are delivered by subscribing to or unsubscribing from notifications.

-   Simple message notifications - These notifications are delivered immediately to the end user, even when the user is chatting with a bot or live agent. The user sees the incoming message but can continue with the current conversation.
-   Actionable notifications - These notifications are delivered only when the user is not in an active conversation with a virtual or live agent. When users complete their conversation with a bot or live agent, they can use the **Show notification** command to view a list of pending notifications, which displays the heading of each notification. Users can select a pending notification to review, then perform the appropriate action for the notification, or skip the action.

## User subscriptions for notifications

End users can subscribe or unsubscribe to notifications on the channel that they're using. For example, the chat menu provides a toggle switch that users can use to subscribe or unsubscribe to notifications on the web channel.

In the conversational integrations for Slack, Microsoft Teams, Workplace from Facebook services, end users manage their notification subscriptions by using the **Subscribe** and **Unsubscribe** commands.

## What to do next

-   **[Create Virtual Agent notifications](../task/create-va-notifications.md)**  
Create a notification that is sent directly to users via the Virtual Agent chatbot. The notification specifies when users receive the notification \(triggers for the notification\) and who receives it \(recipients with and without accounts in the User \[sys\_user\] table\).
-   **[Create additional recipients for Virtual Agent notifications](../task/create-additional-recipients.md)**  
Create and define additional recipients for a Virtual Agent notification to be delivered on chat channels or messaging channels.
-   **[Define Virtual Agent notification contents](../task/define-va-notif-contents.md)**  
Create the content for a Virtual Agent notification delivered in a chat or messaging channel.
-   **[Configure a delivery channel for Virtual Agent notification](../task/configure-delivery-channel.md)**  
Configure a delivery channel for Virtual Agent notifications by specifying the messaging channel information to send notifications to users.
-   **[Define Virtual Agent notification actions](../task/define-va-notif-actions.md)**  
Create the actions for a Virtual Agent chat or messaging channel to send actionable notifications.
-   **[Define the Virtual Agent link actions to notification content](../task/define-va-notif-link-actions.md)**  
Create the link actions for Virtual Agent notification content to be delivered in a chat or messaging channel as actionable notifications.
-   **[Enable Virtual Agent notifications](../task/enable-va-notifications.md)**  
Enable Virtual Agent notifications so that your end users can receive notifications in supported Virtual Agent channels.

**Parent Topic:**[Configuring Virtual Agent](configure-virtual-agent.md)

