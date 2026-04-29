---
title: Activate the Knowledge Management Service Portal plugin
description: The Knowledge Management - Service Portal plugin \(com.snc.knowledge\_serviceportal\) is active by default for customers on Madrid and later releases. Existing customers on release versions prior to Madrid can activate the plugin, if required.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the Knowledge Management Service Portal plugin

The Knowledge Management - Service Portal plugin \(com.snc.knowledge\_serviceportal\) is active by default for customers on Madrid and later releases. Existing customers on release versions prior to Madrid can activate the plugin, if required.

## Before you begin

Role required: admin

## About this task

This plugin requires the following plugins:

-   Knowledge Management V3 \(com.snc.knowledge3\)
-   Service Portal for Enterprise Service Management \(com.glide.service-portal.esm\)

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

