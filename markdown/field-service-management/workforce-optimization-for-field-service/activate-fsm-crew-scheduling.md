---
title: Activate Field Service Crew Operations
description: You can activate the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Crew Operations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Crew Operations

You can activate the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Field Service Crew Operations requires the Field Service Management \[com.snc.work\_management\] plugin. For more information about activating Field Service Management, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md). Ensure that these plugins are activated before you install Field Service Crew Operations.

Role required: admin.

## About this task

The following items are installed with Field Service Crew Operations:

-   Roles
-   Tables
-   Business rules

For more information, see [Field Service Crew Operations components](../reference/crew-scheduling-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

4.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Field Service Crew Operations plugin when activated successfully adds the **sn\_fsm\_crew.work.management.allow.undersized.crew.taskassignment** property to the Field Service Management system properties. For more information, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).

**Previous topic:**[Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md)

**Next topic:**[Activate Field Service Contractor Management](activate-contractor-management-plugin.md)

