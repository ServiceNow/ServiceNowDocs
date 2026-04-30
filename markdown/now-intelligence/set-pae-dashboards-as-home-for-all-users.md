---
title: Set dashboards as home for all users
description: You can set dashboards as home for all users. By default, the most recent dashboard a user has visited is the dashboard they see when they log in to ServiceNow.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-07"
reading_time_minutes: 1
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
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

7.  Set the value to `$pa_dashboard.do`.

8.  Select **Submit**.

    ![User preference form with description, name, type, and value filled in. User field is blank.](../../dashboards/image/user-pref-all-homepages-db.png)


## Result

All users see the last dashboard that they visited when they log in to ServiceNow.

## What to do next

[Set a specific dashboard as home for all users](../../dashboards/task/set-specific-db-as-home-for-all-users.md)

