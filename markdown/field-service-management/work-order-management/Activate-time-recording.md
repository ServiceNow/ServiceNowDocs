---
title: Activate Time Recording for Field Service
description: You can activate the Time Recording for Field Service plugin \(com.snc.wm\_time\_recording\) for Field Service if you have the admin role.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Time Recording, Work order tasks, Work orders and tasks, Configure, Field Service Management]
---

# Activate Time Recording for Field Service

You can activate the Time Recording for Field Service plugin \(com.snc.wm\_time\_recording\) for Field Service if you have the admin role.

## Before you begin

-   Time Recording for Field Service requires the following plugins. Ensure that these plugins are activated before you install Time Recording for Field Service.
    -   **Required ServiceNow plugins**
        -   **Field Service Management \(com.snc.work\_management\)**

            Enables you to manage work requests that are performed on location by field service agents. For information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).


Role required: admin.

## About this task

The following items are installed with Time Recording for Field Service plugin:

-   Plugins
-   Roles

For more information, see [Time Recording for Field Service components](../reference/components-time-recording-fsm.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Time Recording for Field Service plugin \(com.snc.wm\_time\_recording\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


