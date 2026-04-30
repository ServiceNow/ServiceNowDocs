---
title: Set dashboards as home for all users
description: While it is possible for individual users to set dashboards, rather than homepages, you can also set dashboards as home for all users. By default, the most recent dashboard a user has visited is the dashboard they see when they log in to ServiceNow.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set dashboards as home for all users

While it is possible for individual users to set dashboards, rather than homepages, you can also set dashboards as home for all users. By default, the most recent dashboard a user has visited is the dashboard they see when they log in to ServiceNow.

## Before you begin

Role required: admin

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](../concept/homepage-deprecation-help-tool.md) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](../../performance-analytics/concept/analytics-center-dashboards.md).
-   [Working with responsive dashboards](../concept/c_ResponsiveDashboards.md).

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

    ![User preference form with description, name, type, and value filled in. User field is blank.](../image/user-pref-all-homepages-db.png)


## Result

All users see the last dashboard that they visited when they log in to ServiceNow.

## What to do next

[Set a specific dashboard as home for all users](set-specific-db-as-home-for-all-users.md)

