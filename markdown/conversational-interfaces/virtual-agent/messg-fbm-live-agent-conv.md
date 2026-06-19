---
title: Transfer Facebook Messenger chat conversations to live agents
description: Configure the Advanced Work Assignment application to transfer a Facebook Messenger chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/messg-fbm-live-agent-conv.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Transfer, chat, conversation, Live Agent, AWA, Advanced Work Assignment, Facebook, Messenger, Conversational Integration]
breadcrumb: [Use, Conversational Integration with Facebook Messenger, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Transfer Facebook Messenger chat conversations to live agents

Configure the Advanced Work Assignment application to transfer a Facebook Messenger chat conversation initiated by a requester \(customer contact or consumer\) to a live agent.

## Before you begin

Your administrator must have completed the following tasks:

-   [Activate Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/awa-activate.md).
-   [Install Conversational Integration with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/messg-fbm-install.md).
-   Set the application scope to Conversational Integration with Facebook Messenger using the application picker. For more information, see Application picker.
-   Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For more information, see [Activate Conversational Messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/activate-messaging-actions.md).

Role required: admin

## About this task

## Procedure

1.  Enable the Facebook Messenger service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column of the Queues list, search for `Line`.

    3.  Select **Facebook Messenger**.

    4.  On the Service Channel form, select the **Active** check box.

    5.  Select **Update**.

    For more information, see [Service channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/awa-service-channels.md).

2.  Automatically route work items for Facebook Messenger chat conversations to agents by configuring the queue for the Facebook Messenger service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  In the **Name** column of the Queues list, search for `Agent Facebook Messenger Queue`.

    3.  Select **Agent Facebook Messenger Queue**.

    4.  On the Queue form, select the **Active** check box.

    5.  Select **Update**.

    **Note:** By default, the **Facebook Messenger - Most Capacity** assignment rule is associated with the Agent Facebook Messenger Queue. You can create another assignment rule and associate it with the queue. For more information, see [Configure agent assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/awa-create-assignment-rule.md) and [Work item queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/awa-queues.md).

3.  Configure agent presence states for the Facebook Messenger service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  In the **Name** column of the Presence States list, select an existing state.

    3.  On the Presence State form, in the Service channels section, select the add icon &gt; to move the **Facebook Messenger** service channel from the **Available** column to the **Selected** column.

    4.  In the Apply to groups section of the Presence State form, select the add icon &gt; to move the **Agent Facebook Messenger Group** group from the **Available** column to the **Selected** column.

        **Note:** You can ignore this step if you have selected the **Apply to all groups** check box.

    5.  Select **Update**.

    For more information, see [Configure agent presence states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/advanced-work-assignment/awa-configure-agent-presence.md).


**Parent Topic:**[Using Conversational Integration with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/messg-fbm-using.md)

