---
title: Activate Resource Scheduling
description: You can activate the Resource Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Asset Management for Field Service
classification: asset-management-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Scheduling, Inventory and asset management, Configure, Field Service Management]
---

# Activate Resource Scheduling

You can activate the Resource Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Field Service Resource Scheduling requires the Field Service Crew Operations \(com.snc.fsm\_crew\_scheduling\) plugin. For more information about activating Field Service Crew Operations, see [Activate Field Service Crew Operations](activate-fsm-crew-scheduling.md). Ensure that these plugins are activated before you install Field Service Resource Scheduling.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Resource Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

4.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


