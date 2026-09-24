---
title: Set notification preferences
description: Set notification preferences to receive updates via email on the content that you are following.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/manage-subscriptions.html
release: brazil
product: Communities
classification: communities
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Community subscriptions, Using communities, Communities, Customer Service Management]
---

# Set notification preferences

Set notification preferences to receive updates via email on the content that you are following.

## Before you begin

Role required: sn\_communities.community\_user

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## About this task

The Communities application separates the notion of subscriptions from notifications. It is possible to subscribe to an item and disable notifications. You can also turn off all notifications.

## Procedure

1.  Select **Community** &gt; **Notification Settings** from the header.

2.  Click **Notifications and Subscriptions**.

3.  Choose your category, such as **Forums**, **Topics**, **Blogs**, or **Videos**, to manage your notifications in those areas.

4.  In the **Email** column, toggle any item that should or should not send updates.

5.  To turn all notifications on or off, toggle **All Notifications**.

    **Note:**

    Activity subscription modules will not be displayed in the **Navigations and Subscriptions** page, when you enable the disable\_notifications flag.

    The isNotificationDisabled API checks the value of the disable\_notifications flag. This API can also be used for blocking notification of other activity subscription modules.


**Parent Topic:**[Community subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/c_communities-subscriptions.md)

**Related topics**  


[Subscribe to content]()

