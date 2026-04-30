---
title: Activate Template Management for Field Service
description: You can activate the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Template Management, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Activate Template Management for Field Service

You can activate the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Role required: admin

## About this task

Activation of Template Management for Field Service activates the Field Service Management \(com.snc.work\_management\) plugin if it is not already active.

The following items are installed with Field Service Template Management:

-   Tables
-   Script includes
-   Business roles

For more information, see [Template Management for Field Service components](../reference/template-management-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


