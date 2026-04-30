---
title: Activate Field Service Management Access Hours Management
description: You can activate the Field Service Management Access Hours Management plugin \(com.snc.fsm\_access\_hours\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring the auto-population of access hours in a work order task, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Management Access Hours Management

You can activate the Field Service Management Access Hours Management plugin \(com.snc.fsm\_access\_hours\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Field Service Access Hours Management requires the following plugins. Ensure that these plugins are activated before you install Field Service Access Hours Management.
    -   **Required ServiceNow plugins**
        -   **Field Service Management \(com.snc.work\_management\)**

            Enables you to manage work requests that are performed on location by field service agents. For information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).


Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Access Hours Management plugin \(com.snc.fsm\_access\_hours\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Field Service Management Access Hours Management plugin when activated successfully adds the **Access Hours** option to the work order task form.

