---
title: Transfer WhatsApp chat conversations to live agents
description: Configure the Advanced Work Assignment application to transfer a WhatsApp chat conversation initiated by a requester to a live agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Transfer WhatsApp chat conversations to live agents

Configure the Advanced Work Assignment application to transfer a WhatsApp chat conversation initiated by a requester to a live agent.

## Before you begin

Your administrator must have completed the following tasks:

-   [Install Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp-install.md).
-   [Activate Advanced Work Assignment](../../advanced-work-assignment/task/awa-activate.md).
-   Set the application scope to Conversational Integration with WhatsApp \(WhatsApp Cloud API\) using the application picker. For more information, see Application picker.
-   Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For more information, see [Activate Conversational Messaging](activate-messaging-actions.md).

Role required: admin

## About this task

## Procedure

1.  Enable the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column of the Queues list, search for `WhatsApp`.

    3.  Select **WhatsApp**.

    4.  On the Service Channel form, select the **Active** check box.

    5.  Select **Update**.

    For more information, see [Service channels](../../advanced-work-assignment/concept/awa-service-channels.md).

2.  Automatically route work items for WhatsApp chat conversations to agents by configuring the queue for the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  In the **Name** column of the Queues list, search for `Agent WhatsApp Queue`.

    3.  Select **Agent WhatsApp Queue**.

    4.  On the Queue form, select the **Active** check box.

    5.  Select **Update**.

    **Note:** By default, the **WhatsApp - Most Capacity** assignment rule is associated with the Agent WhatsApp Queue. You can create another assignment rule and associate it with the queue. For more information, see [Configure agent assignment rules](../../advanced-work-assignment/task/awa-create-assignment-rule.md) and [Work item queues](../../advanced-work-assignment/reference/awa-queues.md).

3.  Configure agent presence states for the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  In the **Name** column of the Presence States list, select an existing state.

    3.  In the Apply to groups section of the Presence State form, select the add icon to move the **Agent WhatsApp Group** group from the **Available** column to the **Selected** column.

        **Note:** You can ignore this step if you have selected the **Apply to all groups** check box.

    4.  Select **Update**.

    For more information, see [Configure agent presence states](../../advanced-work-assignment/task/awa-configure-agent-presence.md).


**Parent Topic:**[Using Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](../concept/messg-direct-whatsapp-using.md)

