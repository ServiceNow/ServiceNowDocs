---
title: Activate Field Service with Service Locations Support
description: You can activate the Field Service with Service Locations Support \(com.snc.fsm\_service\_locations\) plugin if you have the admin role. The application includes demo data and installs related plugins if they are not already installed.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service with Service Locations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service with Service Locations Support

You can activate the Field Service with Service Locations Support \(com.snc.fsm\_service\_locations\) plugin if you have the admin role. The application includes demo data and installs related plugins if they are not already installed.

## Before you begin

Role required: admin

## About this task

Activation of Field Service with Service Locations Support \(com.snc.fsm\_service\_locations\) plugin activates Field Service Management \(com.snc.work\_management\) and sn-fsm-components \(com.sn\_fsm\_components\) plugins if they are not already active.

For more information, see [Field Service with Service Locations Support components](service-locations-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service with Service Locations Support plugin \(com.snc.fsm\_service\_locations\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


