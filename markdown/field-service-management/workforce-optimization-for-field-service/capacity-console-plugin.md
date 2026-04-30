---
title: Activate Field Service Capacity console
description: You can activate the Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# ActivateField Service Capacity console

You can activate the Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\) for Field Service Management if you have the admin role.

## Before you begin

-   Field Service Advanced Capacity and Reservations management requires the following plugins.
    -   **Required ServiceNow plugins**

        Ensure that these plugins are activated before you install Field Service Advanced Capacity and Reservations management.

        -   Field Service Capacity and Reservations Management \(com.snc.fsm\_capacity\_management\) plugin.
        -   Field Service Territory Planning \(com.snc.fsm\_territory\_planning\) plugin.

Role required: admin.

## About this task

The following components are installed with Field Service Advanced Capacity and Reservations Management plugin:

-   The Capacity Planner role \(fsm\_adv\_cap\_mgmt.wm\_capacity\_planner\) provides read, write, and create access to capacity-related tables, along with access to the Capacity Console.
-   Script Includes: The following table provides the list of script includes that are installed.

    |Name|Description|
    |----|-----------|
    |CapacityConsoleConstants|Aggregate all constants in one place for the Capacity Console. Customers can override constants from `CapacityConsoleConstantsSNC`.|
    |CapacityConsoleConstantsSNC|Aggregate all constants in one place for the Capacity Console.|
    |CapacityConsoleData|Contains all the business logic for the Capacity Console. Customers can override this logic using `CapacityConsoleDataSNC`.|
    |CapacityConsoleDataSNC|Contains all the business logic for the Capacity Console.|
    |CapacityConsoleUtil|Contains all utility functions for the Capacity Console.|
    |CapacityConsoleUtilSNC|Contains all utility functions for the Capacity Console.|
    |FSMCapacityAdvancedFilterDefinition|Custom implementation of all advanced filters used in the Capacity Console.|


**Note:** You can customize the Capacity Console by taking the reference from the SNC script includes.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Advanced Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Capacity Console](../concept/capacity-console.md)

[Using the Capacity Console](../concept/capacity-and-reservation-management-console.md)

