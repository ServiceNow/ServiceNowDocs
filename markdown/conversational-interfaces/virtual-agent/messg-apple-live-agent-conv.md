---
title: Transfer Apple Messages for Business chat conversations to live agents
description: Configure the Advanced Work Assignment application to transfer a Apple Messages for Business chat conversation initiated by a requester to a live agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Virtual Agent, Transfer, conversation, Live Agent, apple, messages, advanced work assignment, AWA]
breadcrumb: [Use, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Transfer Apple Messages for Business chat conversations to live agents

Configure the Advanced Work Assignment application to transfer a Apple Messages for Business chat conversation initiated by a requester to a live agent.

## Before you begin

Your administrator must have completed the following tasks:

-   [Activate Advanced Work Assignment](../../advanced-work-assignment/task/awa-activate.md).
-   Set the application scope to Conversational Integration with Apple Messages for Business using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).
-   Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For more information, see [Activate Conversational Messaging](activate-messaging-actions.md).

Role required: admin

## About this task

![A conversation with a virtual agent on an iPhone.](../images/iMessage-apps.png "Messaging with a virtual agent")

![A conversation with a live agent on an iPhone.](../images/amb-rich-links.png "Messaging with a live agent")

## Procedure

1.  Enable the Apple Messages for Business service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column of the Queues list, search for `Apple Messages for Business`.

    3.  Select **Apple Messages for Business**.

    4.  On the Service Channel form, select the **Active** check box.

    5.  Select **Update**.

    6.  Add agents to the `Agent Apple Messages for Business Queue`.

    For more information, see [Service channels](../../advanced-work-assignment/concept/awa-service-channels.md).

2.  Automatically route work items for Apple Messages for Business chat conversations to agents by configuring the queue for the Apple Messages for Business service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  In the **Name** column of the Queues list, search for `Apple Messages for Business Queue`.

    3.  Select **Agent Apple Messages for Business Queue**.

    4.  On the Queue form, select the **Active** check box.

    5.  Select **Update**.

    **Note:** By default, the **Apple Messages for Business - Most Capacity** assignment rule is associated with the Agent Apple Messages for Business Queue. You can create another assignment rule and associate it with the queue. For more information, see [Configure agent assignment rules](../../advanced-work-assignment/task/awa-create-assignment-rule.md) and [Work item queues](../../advanced-work-assignment/reference/awa-queues.md).

3.  Configure agent presence states for the Apple Messages for Business service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  In the **Name** column of the Presence States list, select an existing state.

    3.  In the Apply to groups section of the Presence State form, select the add icon &gt; to move the **Agent Apple Messages for Business Group** group from the **Available** column to the **Selected** column.

        **Note:** You can ignore this step if you have selected the **Apply to all groups** check box.

    4.  Select **Update**.

    For more information, see [Configure agent presence states](../../advanced-work-assignment/task/awa-configure-agent-presence.md).


