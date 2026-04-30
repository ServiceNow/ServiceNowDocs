---
title: Set up HR Service Delivery Conversational SMS service channel
description: Configure the Conversational SMS service channel store app for HR Service Delivery.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SMS conversations, Use, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Set up HR Service Delivery Conversational SMS service channel

Configure the Conversational SMS service channel store app for HR Service Delivery.

## Before you begin

Role required: admin

## About this task

The HR Service Delivery base system includes the **HR SMS** service channel queue with the default **HR SMS Support Group** assignment group. The **Agent assignment rule** is capacity based by default. For HR Service Delivery, configure the SMS service channel for the HR SMS queue.

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.

2.  Click the **SMS** service channel.

3.  On the Service Channel SMS form, select the **Active** check box to activate the service channel.

    **Note:** By default, most of the form is populated for you. **Capacity and Utilization** fields are set to 1 for **Default work item size** and 4 for **Default capacity**. You can change these, and any form values, if desired.

    ![HR SMS Service Channel SMS form](../image/setup-hr-sms-service-channel.png)

4.  Click the Queues related list to view and configure the HR SMS queue.

    ![HR SMS Queues related list](../image/Queues-related-list-hr-sms.png)

5.  View the default configurations on the Queue HR SMS form, ensuring the **Active** check box is checked.

6.  Modify values as you desire.

    ![Queue HR SMS form configuration](../image/hr-sms-queue-configuration.png)

7.  Click on any of the related lists to view or modify default configured values.

    **Note:** Notice that the Assignment Eligibility related list defaults to the **HR SMS Support Group**. Manually add users to this group to route assignments. Refer to [Add a user to a group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to learn how to add users to this group.

8.  Click **Update** to save any changes you made.

9.  Update the Advanced Work Assignment Presence States by navigating to **Advanced Work Assignment** &gt; **Settings** &gt; **Presence States**.

10. Click **Available** in the Presence States list.

11. In the Presence State Available form, select **SMS** in the **Service channels Available** column and move it to the **Selected** column using the right-pointing arrow.

    ![HR SMS Advanced Work Assignment Presence States configuration](../image/sms-hr-presence-state-config.png)

12. Click **Update**.

    **Note:** For complete information regarding Conversational SMS service channels and setup guidance, refer to [Conversational SMS service channel](https://www.servicenow.com/docs/access?context=conversation-sms-service-channel-store-app&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


