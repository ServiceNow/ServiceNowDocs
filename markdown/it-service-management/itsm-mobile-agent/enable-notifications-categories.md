---
title: Enable push notification categories for ITSM Mobile Agent
description: Enable push notification categories so your users can turn on or turn off notifications by category.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/enable-notifications-categories.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# Enable push notification categories for ITSM Mobile Agent

Enable push notification categories so your users can turn on or turn off notifications by category.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  In the system properties list, find and open the property with the name **com.glide.sg.notifications.management**.

    **Note:** If the property doesn't exist, select **New** and create a true\|false property with the name mentioned in the previous step. After changing this property, users must log out and then log back in for the change to take effect.

3.  In the **Value** field, enter `true`.

4.  Select **Update**.

    \[Omitted image "notification-category-selection1.png"\] Alt text: Notification selection\[Omitted image "notification-category-selections2.png"\] Alt text: Notifications by category

    Users can turn on or turn off notifications by category. The categories shown in the notification preferences screen are defined in the Notifications \[sysevent\_email\_action\] table. The first image shows all the reference categories defined on this table. The second image shows the record matching the selected category.

    After you update the system property, users can turn on or turn off notifications by the defined categories.


