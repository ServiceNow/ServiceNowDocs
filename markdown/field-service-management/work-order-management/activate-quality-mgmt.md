---
title: Activate Field Service Quality Management
description: You can activate the Field Service Quality Management plugin \(com.sn\_fsm\_quality\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Quality Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Quality Management

You can activate the Field Service Quality Management plugin \(com.sn\_fsm\_quality\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Field Service Quality Management requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

The following items are installed with Field Service Quality Management:

-   Tables
-   Substates
-   Roles

For more information, see [Field Service Quality Management components](../reference/quality-mgmt-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Quality Management plugin \(com.sn\_fsm\_quality\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Field Service Quality Management](../concept/quality-management-fsm.md)

[Review a task](review-send-task-back.md)

[Respond to a reviewed task](../concept/close-wo-wot-mobile.md#)

[Field Service Quality Management components](../reference/quality-mgmt-components.md)

