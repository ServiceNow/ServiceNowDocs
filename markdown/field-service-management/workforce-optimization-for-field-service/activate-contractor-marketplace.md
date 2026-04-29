---
title: Activate Field Service Marketplace
description: You can activate the Field Service Marketplace plugin \( com.snc.fsm\_marketplace\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data if they aren’t already installed.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Marketplace, Contractor capabilities, Set up workforce, Configure, Field Service Management]
---

# Activate Field Service Marketplace

You can activate the Field Service Marketplace plugin \(com.snc.fsm\_marketplace\) for Field Service Management if you have the admin role. The application includes demo data if they aren’t already installed.

## Before you begin

Role required: admin

## About this task

The following items are installed with Field Service Marketplace:

-   Tables
-   Roles
-   System properties
-   Business rules
-   Script includes

For more information, see [Field Service Marketplace components](../reference/contractor-marketplace-cmpnts.md).

**Note:** To utilize automation in Field Service Marketplace, the Dynamic Scheduling plugin must be installed and the **Use task filters for determining contractor tasks** property must be enabled.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Marketplace plugin \(com.snc.fsm\_marketplace\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


