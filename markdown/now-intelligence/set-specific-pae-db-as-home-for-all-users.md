---
title: Set a specific Platform Analytics dashboard as home for all users
description: Configure ServiceNow so that all users see the same dashboard when they log in.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set dashboards as home for all users, Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Set a specific Platform Analytics dashboard as home for all users

Configure ServiceNow so that all users see the same dashboard when they log in.

## Before you begin

Role required: admin

**Note:** Navigate to the dashboard you want to set as home, and copy the sys\_id from the URL. The sys\_id is the last element after the last forward slash. For example, in this URL, the sys\_id is 456CBA: `https://my-instance.service-now.com/now/platform-analytics-workspace/dashboards/params/edit/false/sys-id/456CBA`. Paste the sys\_id into a text file so that you can copy it into the system preference you create.

## About this task

The dashboard that you configure should be available to all users.

## Procedure

1.  Create a user preference with the name `my_home_navigation_page`.

2.  Give the preference the description `Set all homepages to dashboards`.

3.  Select the **System** check box to create an instance-wide default.

4.  Leave the **User** field empty.

    Steps 3 and 4 make the preference universal.

5.  Give the preference a meaningful description that you can search for.

6.  Set the **Type** to `string`.

7.  In the **Value** field, enter the following: `$pa_dashboard.do?sysparm_dashboard=dashboard_sys_id`, but replace `dashboard_sys_id` with the sys\_id you copied before you began.

8.  Select **Submit**.


## Result

All users see the same dashboard when they open ServiceNow.

