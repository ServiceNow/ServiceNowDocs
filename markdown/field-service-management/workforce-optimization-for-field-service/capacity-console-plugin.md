---
title: Activate Field Service Advanced Capacity and Reservations management
description: You can activate the Field Service Advanced Capacity and Reservations management \(com.snc.fsm\_advanced\_capacity\_management\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/workforce-optimization-for-field-service/capacity-console-plugin.html
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# ActivateField Service Advanced Capacity and Reservations management

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

-   Tables
-   Script Includes
-   Roles

For more information, see [Capacity and Reservations Management components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/advanced-capacity-components.md).

**Note:** You can customize the Capacity Console by taking the reference from the SNC script includes.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Advanced Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


**Related topics**  


[Capacity Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/capacity-console.md)

[Using the Capacity Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-manager-workforce/capacity-and-reservation-management-console.md)

