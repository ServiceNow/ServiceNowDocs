---
title: Enable Self-Service online check-in for Walk-up Experience
description: Show or hide the Walk-up Experience online Walk-up Check-in module under Self-Service in the application navigator. You can enable or disable the module using the basic platform menu or module enablement process.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Enable Self-Service online check-in for Walk-up Experience

Show or hide the Walk-up Experience online **Walk-up Check-in** module under **Self-Service** in the application navigator. You can enable or disable the module using the basic platform menu or module enablement process.

## Before you begin

Role required: sn\_walkup.walkup\_admin or admin

## About this task

The Walk-up Experience online **Walk-up Check-in** module is disabled \(hidden\) by default and does not appear under the **Self-Service** menu until enabled.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Click **All** in the conditions breadcrumbs to display both active and inactive application menus.

    This action removes the default filter condition.

3.  Search by **Title** for the **Self-Service** application menu.

    Search yields the itil\_self\_service and mobile\_self\_service menu applications. You can enable \(show\) the **Walk-up Check-in** module for each menu application.

4.  Click the **Self-Service** menu application with the **Name:** **itil\_self\_service**.

    The application menu Self-Service record opens and the Modules related list shows the modules that appear in the application navigator.

5.  Search by **Title** for the **Walk-up Check-in** module.

6.  Click **Walk-up Check-in**.

    The **Walk-up Check-in** module record opens.

7.  In the **Visibility** tab, click **Active** to enable the **Walk-up Check-in** module.

    Active is **true** for the module. Alternatively, you can enable the module from the **Applications Menus Self-Service** Modules related list:

    1.  Double-click the **Active** field beside the **Walk-up Check-in** module name in the Modules related list.

    2.  Set **Active** to **true** \(show\) or **false** \(hide\).

8.  Click **Update**.

    When you change application menus or modules, the application navigator automatically refreshes to display the changes.

9.  To enable the **Walk-up Check-in** module to display under **Self-Service** on the mobile application, click **Walk-up Check-in** in the Mobile Modules related list.

10. Click the **Active** field to enable the module for mobile devices.

11. Click **Update**.


**Parent Topic:**[Configuring Walk-up Experience](../concept/walkup-experience-configuration.md)

