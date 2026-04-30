---
title: Transfer WhatsApp chat conversations to live agents
description: Configure the Advanced Work Assignment application to transfer a WhatsApp chat conversation initiated by a requester to a live agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 1
keywords: [Transfer, Whatsapp, Live agent, Advanced Work Assignment, AWA, Twilio, Service channels, Application picker, Conversational Messaging]
breadcrumb: [Configure Conversational Integration with WhatsApp \(powered by Twilio\), Conversational Integration with WhatsApp \(powered by Twilio\), Integrating Virtual Agent with consumer messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Transfer WhatsApp chat conversations to live agents

Configure the Advanced Work Assignment application to transfer a WhatsApp chat conversation initiated by a requester to a live agent.

## Before you begin

Your administrator must have completed the following tasks:

-   [Install Conversational Integration with WhatsApp \(powered by Twilio\)](messg-whatsapp-install.md).
-   [Activate Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-activate&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   Set the application scope to Conversational Integration with WhatsApp \(powered by Twilio\) using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Activate the Conversational Messaging plugin \(com.glide.messaging.awa\). For more information, see [Activate Conversational Messaging](https://www.servicenow.com/docs/access?context=activate-messaging-actions&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: admin

## About this task

## Procedure

1.  Enable the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Service Channels**.

    2.  In the **Name** column of the Queues list, search for `WhatsApp`.

    3.  Select **WhatsApp**.

    4.  On the Service Channel form, select the **Active** check box.

    5.  Select **Update**.

    For more information, see [Service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

2.  Automatically route work items for WhatsApp chat conversations to agents by configuring the queue for the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

    2.  In the **Name** column of the Queues list, search for `Agent WhatsApp Queue`.

    3.  Select **Agent WhatsApp Queue**.

    4.  On the Queue form, select the **Active** check box.

    5.  Select **Update**.

    **Note:** By default, the **WhatsApp - Most Capacity** assignment rule is associated with the Agent WhatsApp Queue. You can create another assignment rule and associate it with the queue. For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Work item queues](https://www.servicenow.com/docs/access?context=awa-queues&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

3.  Configure agent presence states for the WhatsApp service channel.

    1.  Navigate to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

    2.  In the **Name** column of the Presence States list, select an existing state.

    3.  In the Apply to groups section of the Presence State form, select the add icon &gt; to move the **Agent WhatsApp Group** group from the **Available** column to the **Selected** column.

        **Note:** You can ignore this step if you have selected the **Apply to all groups** check box.

    4.  Select **Update**.

    For more information, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


