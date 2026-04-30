---
title: Set notification preferences
description: Set notification preferences to receive updates via email on the content that you are following.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Community subscriptions, Use a community, Communities, Customer Service Management]
---

# Set notification preferences

Set notification preferences to receive updates via email on the content that you are following.

## Before you begin

Role required: sn\_communities.community\_user

## About this task

The Communities application separates the notion of subscriptions from notifications. It is possible to subscribe to an item and disable notifications. You can also turn off all notifications.

## Procedure

1.  On the Community homepage, click **Community** &gt; **Notification Settings**.

2.  Click **Notification Preferences**.

3.  To manage your notifications in those areas, choose your category, such as **Forums**, **Topics**, **Blogs**, or **Videos**.

    Choose the **Network** category and then choose **View Network** to view the community users, who are following you, or the community users that you are following.

4.  In the **Email** column, toggle any item that should or should not send updates.

5.  To turn all notifications on or off, toggle **Receive Notifications**.

    **Note:**

    Activity subscription modules will not be displayed in the Navigations and Subscriptions page, when you enable the disable\_notifications flag.

    The isNotificationDisabled API checks the value of the disable\_notifications flag. This API can also be used for blocking notification of other activity subscription modules.


**Parent Topic:**[Community subscriptions](../concept/c_communities-subscriptions.md)

**Related topics**  


[Subscribe to content](subscribe.md)

