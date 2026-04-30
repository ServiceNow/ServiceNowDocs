---
title: Install External Legal Service Center
description: You can activate the External Legal Service Center plugin \(sn\_lg\_ext\_portal\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: External Legal Portal
classification: external-legal-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring up External Legal Service Center, External Legal Service Center, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Install External Legal Service Center

You can activate the External Legal Service Center plugin \(sn\_lg\_ext\_portal\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

External Legal Service Center requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate this feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

Required plugins and roles are installed with External Legal Service Center.

For more information, see [External Legal Service Center reference](../concept/lsd-ext-portal-reference-landing.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the External Legal Service Center plugin \(sn\_lg\_ext\_portal\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


