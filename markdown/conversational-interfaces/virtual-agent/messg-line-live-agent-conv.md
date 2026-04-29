---
title: Transfer LINE chat conversations to live agents
description: Configure the Advanced Work Assignment application to transfer a LINE chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Transfer, LINE, chat, conversations, Live Agent, AWA, Advanced Work Assignment, Conversational, Messaging, Integration]
breadcrumb: [Use, Conversational Integration with LINE, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Transfer LINE chat conversations to live agents

Configure the Advanced Work Assignment application to transfer a LINE chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.

## Before you begin

Your administrator must have completed the following tasks:

-   [Activate Advanced Work Assignment](../../advanced-work-assignment/task/awa-activate.md).
-   [Install Conversational Integration with LINE](messg-line-install.md).
-   Set the application scope to Conversational Integration with LINE using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).
-   Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For more information, see [Activate Conversational Messaging](activate-messaging-actions.md).

Role required: admin

## About this task

## Procedure

1.  Enable the Line service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column of the Queues list, search for `Line`.

    3.  Select **Line**.

    4.  On the Service Channel form, select the **Active** check box.

    5.  Select **Update**.

    For more information, see [Service channels](../../advanced-work-assignment/concept/awa-service-channels.md).

2.  Automatically route work items for LINE chat conversations to agents by configuring the queue for the Line service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  In the **Name** column of the Queues list, search for `Agent Line Queue`.

    3.  Select **Agent Line Queue**.

    4.  On the Queue form, select the **Active** check box.

    5.  Select **Update**.

    **Note:** By default, the **Line - Most Capacity** assignment rule is associated with the Agent Line Queue. You can create another assignment rule and associate it with the queue. For more information, see [Configure agent assignment rules](../../advanced-work-assignment/task/awa-create-assignment-rule.md) and [Work item queues](../../advanced-work-assignment/reference/awa-queues.md).

3.  Configure agent presence states for the Line service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  In the **Name** column of the Presence States list, select an existing state.

    3.  On the Presence State form, in the Service channels section, select the add icon &gt; to move the **Line** service channel from the **Available** column to the **Selected** column.

    4.  In the Apply to groups section of the Presence State form, select the add icon &gt; to move the **Agent Line Group** group from the **Available** column to the **Selected** column.

        **Note:** You can ignore this step if you have selected the **Apply to all groups** check box.

    5.  Select **Update**.

    For more information, see [Configure agent presence states](../../advanced-work-assignment/task/awa-configure-agent-presence.md).


**Parent Topic:**[Using Conversational Integration with LINE](../concept/messg-line-using.md)

