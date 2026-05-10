---
title: Activate Sidebar for the Field Service Mobile Agent application
description: You can activate the Sidebar for Field Service Management plugin \(sn\_fsm\_sidebar\) for Field Service Management if you have the admin role. Activating this plugin enables the Sidebar feature on the Mobile Agent application.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Activate Sidebar for the Field Service Mobile Agent application

You can activate the Sidebar for Field Service Management plugin \(sn\_fsm\_sidebar\) for Field Service Management if you have the admin role. Activating this plugin enables the Sidebar feature on the Mobile Agent application.

## Before you begin

Role required: admin

**Note:** Sidebar is a ServiceNow AI Platform® capability. For more information on configuring Sidebar, see [Configuring Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/configure-sidebar.md).

For more information on how Sidebar works, see [Exploring Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/exploring-sidebar.md).

## About this task

Activating this plugin enables the Sidebar feature on the Mobile Agent application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Sidebar for Field Service Management plugin \(sn\_fsm\_sidebar\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Start a Sidebar discussion on the Mobile Agent application](start-sidebar-mobile.md)

[Summarize a Sidebar discussion on the ServiceNow Agent application](na-fsm-summarize-sidebar-platform.md#)

