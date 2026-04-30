---
title: Activate Field Service Territory Planning
description: You can activate the Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Territory Planning

You can activate the Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\) for Field Service Management if you have the admin role. The application includes demo data and installs related applications and plugins if they are not already installed.

## Before you begin

Field Service Territory Planning requires the installation of Dispatcher Workspace plugin \(com.snc.uib.fsm\_dispatcher\_workspace\) to access the Territory Planning console.

Role required: admin

## About this task

Activation of Field Service Territory Planning activates Field Service Management \(com.snc.work\_management\) and Territory Planning \(com.snc.territory\_planning\) plugins if they are not already active.

The following items are installed with Field Service Territory Planning:

-   Roles
-   Tables
-   Script includes
-   Business rules
-   Properties
-   Query rules

For more information, see [Field Service Territory Planning components](../reference/territory-planning-components-fsm.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Field Service Territory Planning plugin when activated successfully adds the default territory model, Field\_Service\_Territories to the Field Service configurations, inside the Add-ons tab.

**Note:** You must activate the **Field\_Service\_Territories** model after setting up your territories to schedule work order tasks based on territories. For more information, see [Enable the Field Service territory model](enable-territory-model.md).

