---
title: Find components installed with an application
description: Activating a plugin installs an application on your instance. Each application consists of components such as tables, user roles, and scheduled jobs. To view all components that are installed with an application, see the Application Files table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Find components installed with an application

Activating a plugin installs an application on your instance. Each application consists of components such as tables, user roles, and scheduled jobs. To view all components that are installed with an application, see the Application Files table.

## Before you begin

-   The application plugin must be activated.
-   Roles required: admin or the application admin role

    **Note:** The application admin role is only required for applications that use the Application administration feature. For example, Vulnerability Response.


## About this task

In the Application Files table, look up the components that are installed with the plugin for the application. If the application comprises multiple plugins, look up each plugin individually.

## Procedure

1.  In the navigation filter, enter: `sys_metadata.list`

    The list of Application Files records is displayed.

2.  Click the personalize list icon \(![gear icon](../../../common/image/gear.png)\), and add the **Package** column to the list.

3.  Filter the list with these conditions to show only the components for the plugin:

    **\[Package\] \[is\] \[ _&lt;plugin name&gt;_\]**

4.  In the **Class** column heading, click the menu icon \(![menu icon](../image/HamburgerMenu.png)\) and select **Group by Class**.

5.  Select the class of information that you want to view.


**Parent Topic:**[Basic system configuration](../../core-configuration/concept/p_CoreConfigurationOverview.md)

