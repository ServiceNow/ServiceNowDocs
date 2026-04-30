---
title: Restrict responsive dashboard sharing by role
description: You can configure responsive dashboard properties to restrict which users are able to share responsive dashboards.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Restrict responsive dashboard access to specific roles, Dashboard permissions, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Restrict responsive dashboard sharing by role

You can configure responsive dashboard properties to restrict which users are able to share responsive dashboards.

## Before you begin

Role required: admin.

## About this task

Configure a dashboard property to specify a comma-separated list of roles that can share their own dashboards. Users with these roles can see the **Share** icon \(![](../image/SharingIcon.png)\) on responsive dashboards.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Dashboard Properties**.

2.  In the field labeled **List of roles \(comma-separated\) that can share their own dashboards**, enter the roles.

    For example, if all users with the itil, asset, and pa\_admin roles can share dashboards, enter `itil, asset, pa_admin`. If this field is empty, users with any role can share their own dashboards.

    **Note:** If one role in this list is misspelled, that role will not be able to share dashboards. If there is only one role in this list and that role is misspelled, no user will be able to share dashboards until the value for this property is corrected.


## Result

Users with the specified roles can see the **Share** panel when they view a dashboard that they own. Users with other roles are not able to see the **Share** panel.

**Note:** Properties that restrict dashboard sharing do not apply to users with the admin and dashboard\_admin roles. Users with these two roles can always share any dashboard.

## What to do next

To apply security rules to what is visible in the **Share** panel, select the box labeled **Apply security rules to the list of users, user groups, and roles that are visible when sharing dashboards**. For more information, see [Restrict responsive dashboard sharing with security rules](restrict-responsive-db-sharing-w-security-rule.md).

**Related topics**  


[Share a responsive dashboard](t_ControlAccessToADashboard.md)

