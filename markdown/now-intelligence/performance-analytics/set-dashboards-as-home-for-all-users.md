---
title: Set dashboards as home for all users
description: You can set dashboards as home for all users. By default, the most recent dashboard a user has visited is the dashboard they see when they log in to ServiceNow.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set dashboards as home for all users

You can set dashboards as home for all users. By default, the most recent dashboard a user has visited is the dashboard they see when they log in to ServiceNow.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Create a user preference with the name `my_home_navigation_page`.

3.  Give the preference the description `Set all homepages to dashboards`.

4.  Select the **System** check box to create an instance-wide default.

5.  Leave the **User** field empty.

    Steps 4 and 5 make the preference universal.

6.  Set the **Type** to `string`.

7.  Set the value to `/now/platform-analytics-workspace/dashboards`.

8.  Select **Submit**.

    ![User preference form with description, name, type, and value filled in. User field is blank.](../image/user-pref-all-homepages-db.png)


## Result

All users see the last dashboard that they visited when they log in to ServiceNow.

## What to do next

[Set a specific dashboard as home for all users](set-specific-db-as-home-for-all-users.md)

