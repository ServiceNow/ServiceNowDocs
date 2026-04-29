---
title: Activate Field Service Work Configurations
description: You can activate the Field Service Work Configurations plugin \(com.snc.fsm\_work\_types\) for Field Service Management if you have the admin role. Activating Work Configurations enables you to define configurations for a specific type of work, ensuring consistency.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work Configurations, Set up work orders and tasks, Configure, Field Service Management]
---

# Activate Field Service Work Configurations

You can activate the Field Service Work Configurations plugin \(com.snc.fsm\_work\_types\) for Field Service Management if you have the admin role. Activating Work Configurations enables you to define configurations for a specific type of work, ensuring consistency.

## Before you begin

Role required: admin

## About this task

Install the Field Service Work Configurations plugin \(com.snc.fsm\_work\_types\) to activate Field Service Work Configurations. Optionally, install the Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin for an example Field Service Work Configurations workflow. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed. For more information on the components installed with the plugins, see [Field Service Work Configurations components](../reference/work-configuration-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Work Configurations plugin \(com.snc.fsm\_work\_types\) and an optional Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


