---
title: Create the notification for the Asset Refresh topic
description: Create an actionable notification to trigger the Asset Refresh Virtual Agent example topic you just created. The user will automatically receive the notification when it's time for them to order a new hardware asset.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-12"
reading_time_minutes: 2
keywords: [Create, notification, Asset Refresh, topic, Virtual Agent]
breadcrumb: [Example Asset Refresh Virtual Agent conversation with notifications, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create the notification for the Asset Refresh topic

Create an actionable notification to trigger the Asset Refresh Virtual Agent example topic you just created. The user will automatically receive the notification when it's time for them to order a new hardware asset.

## Before you begin

Publish the Asset Refresh topic. [Change the application scope](change-application-scope-vad.md) in your instance to the same application you used to create your Asset Refresh topic. Ideally, the notification should be in the same application scope as your Virtual Agent topic.

Role required: virtual\_agent\_admin or admin

## About this task

The ServiceNow AI Platform and ITSM Virtual Agent Conversations come with pre-built actionable notifications, and you can also create your own. For more information, see [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Tip:** On the Notifications page, you can view only the actionable notifications that come with ITSM Virtual Agent Conversations by filtering the list on **Application is ITSM Virtual Agent Conversations**.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select **New**.

3.  In the **Name** field, provide a unique name, such as `Asset Refresh Notification`.

4.  On the **When to send** tab, specify the trigger that will send the notification.

    1.  For the Trigger, specify **Record Change**.

    2.  For the Table, specify the **Hardware \[alm\_hardware\]**.

    3.  For the Conditions, specify **State &gt; is &gt; In maintenance**.

        When assets in the hardware table are available for refresh, they're moved to the **In maintenance** state on this example instance. You can specify filter conditions based on the business rules for your instance.

    ![A change in state for the asset on the Hardware table will trigger this notification.](../images/crawl-ex-new-notification.png)

5.  Select the **Who will receive** tab to configure the recipient of the notification.

    1.  Select the lock icon next to **Recipients listed in fields**.

    2.  In the **Available** list, select **Assigned to**, and then select the right arrow icon to move it to the **Selected** column.

    ![The notification will only be sent to the owner of the asset.](../images/crawl-ex-notif-who-receives.png)

6.  Select **Submit**.


## What to do next

[Associate content with the Asset Refresh notification](associate-content-example-notification.md)

**Related topics**  


[ITSM Virtual Agent pre-built actionable notifications](https://www.servicenow.com/docs/access?context=itsm-actionable-notifications&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

