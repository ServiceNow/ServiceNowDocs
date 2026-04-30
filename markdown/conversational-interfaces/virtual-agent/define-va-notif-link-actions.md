---
title: Define the Virtual Agent link actions to notification content
description: Create the link actions for Virtual Agent notification content to be delivered in a chat or messaging channel as actionable notifications.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Virtual Agent notifications, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Define the Virtual Agent link actions to notification content

Create the link actions for Virtual Agent notification content to be delivered in a chat or messaging channel as actionable notifications.

## Before you begin

-   Ensure that you have activated the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

    **Note:** Only Virtual Agent Pro customers can associate actions with notification contents and receive actionable notifications.

-   Role required: virtual\_agent\_admin or admin.

## About this task

Notification content, with no associated link actions, is delivered as a non-actionable notification.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications** and select the notification for which you're defining the link actions.

2.  In the Link Actions related list, select **New**.

3.  On the form, fill in the fields.

<table id="table_jbc_wtb_lpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the link action.

</td></tr><tr><td>

Actions

</td><td>

Notification action that the link action is created to.You can select one or more notification actions for a notification and also put them in the order that you want them to be shown on the notification.

</td></tr><tr><td>

Actions listed in event parm1

</td><td>

Actions listed in an event parameter.Users and actions cannot both be passed into the parameter. For example, if you input a sys\_id of a user in event param1, the user is considered in the output.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification content.

</td></tr><tr><td>

Notification

</td><td>

Notification that is associated with the content. This field is populated automatically with the notification that you created.

</td></tr><tr><td>

Content

</td><td>

Notification content for the link action created.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification content.

</td></tr><tr><td>

Actions listed in event parm2

</td><td>

Actions listed in an event parameter.Users and actions cannot both be passed into the parameter. For example, if you input a sys\_id of a user in event param2, the user is considered in the output.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  To define another link action for the notification content, repeat steps 3 and 4.

    **Note:** Only a single notification with active content is supported for a provider. However, if the content for the notification is not active, you can define the secondary content for the notification and make that content active.

6.  To remove the **Skip** action from an actionable notification, do the following steps:

    1.  Select the notification and open the Link Actions to Content related list.

    2.  Select the Actionable Content and select the **Disable skip** option.

        **Note:** This option only displays when the Content Type is Virtual Agent.


## What to do next

Enable Virtual Agent notifications. For more information, see [Enable Virtual Agent notifications](enable-va-notifications.md).

**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)

