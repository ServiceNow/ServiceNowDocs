---
title: Activate Field Service Capacity and Reservations Management
description: You can activate the Field Service Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Capacity and Reservations Management

You can activate the Field Service Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) for Field Service Management if you have the admin role.

## Before you begin

-   Field Service Capacity and Reservations Management requires the following plugins. Ensure that these plugins are activated before you install Field Service Capacity and Reservations Management.
    -   **Required ServiceNow plugins**
        -   **Field Service Management \(com.snc.work\_management\)**

            For more information about activating Field Service Management, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).


Role required: admin.

## About this task

The following items are installed with Field Service Capacity and Reservations Management:

-   Tables
-   Business Rules

For more information, see [Field Service Capacity and Reservations Management components](../reference/capacity-management-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


