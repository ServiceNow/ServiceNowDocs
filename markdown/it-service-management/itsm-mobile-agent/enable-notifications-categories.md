---
title: Enable Push notification categories for ITSM Mobile Agent
description: Enable push notification categories so your users can enable or disable notifications by category.
locale: en-US
release: yokohama
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, ITSM Mobile Agent, IT Service Management]
---

# Enable Push notification categories for ITSM Mobile Agent

Enable push notification categories so your users can enable or disable notifications by category.

## Before you begin

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the application navigator.

2.  In the system properties list, find and open the property with the name **com.glide.sg.notifications.management**.

    **Note:** If the property does not exist, click **New** and create a true\|false property with the name mentioned in the previous step. After changing this property, users must log out and then log back in for the change to take effect.

3.  In the **Value** field, enter `true`.

4.  Select **Update**.

    ![Notifications by category](../image/notification-category-selection.png)

    The user can enable or disable notifications by category. The categories shown in the notification preferences screen are defined in the **Notifications** \[sysevent\_email\_action\] table. The screen to the left shows all the reference categories defined on this table. The screen to the right shows the record matching the selected category.

    After you have updated your system property, your users will be able to enable or disable notifications by the defined categories.


