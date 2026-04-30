---
title: Set a specific Platform Analytics dashboard as home for specific users
description: Configure ServiceNow so that specified users see the same dashboard when they log in.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set dashboards as home for all users, Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Set a specific Platform Analytics dashboard as home for specific users

Configure ServiceNow so that specified users see the same dashboard when they log in.

## Before you begin

Role required: admin

**Note:** Navigate to the dashboard you want to set as home, and copy the sys\_id from the URL. The sys\_id is the last element after the last forward slash. For example, in this URL, the sys\_id is 456CBA: `https://my-instance.service-now.com/now/platform-analytics-workspace/dashboards/params/edit/false/sys-id/456CBA`. Paste the sys\_id into a text file so that you can copy it into the system preference you create.

## About this task

The dashboard that you configure should be available to all users.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Create a user preference with the name `my_home_navigation_page`.

3.  Give the preference a meaningful description such as `Set home dashboard for ITIL users` that users can search for.

4.  In the **User** field, specify one user this dashboard will be the home for.

5.  Set the **Type** to `string`.

6.  In the **Value** field, enter the following: `$pa_dashboard.do?sysparm_dashboard=dashboard_sys_id`, but replace `dashboard_sys_id` with the sys\_id you copied before you began.

7.  Select **Submit**.

8.  Select the context menu \(![Context menu icon](../../../common/image/Form_MenuIcon.png)\) and choose **Insert and Stay**.

    This action duplicates the user preference so that you can specify another user this dashboard will be home for. You can also specify a different sys\_ID on the duplicated record.


## Result

The specified users see the specified dashboards when they open ServiceNow or select the company logo.

