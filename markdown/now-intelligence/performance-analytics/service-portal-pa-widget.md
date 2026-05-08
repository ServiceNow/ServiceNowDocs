---
title: Performance Analytics widgets on Service Portal
description: You can show Performance Analytics indicators and breakdowns using Service Portal.You can activate the Performance Analytics and Reporting - Service Portal Widgets plugin \(com.snc.pa.sp.widget\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Performance Analytics widgets on Service Portal

You can show Performance Analytics indicators and breakdowns using Service Portal.

When you edit a portal, add the **Performance Analytics** widget. Use the widget options to select an existing Performance Analytics widget to show on the portal and whether to show its title.

![Performance Analytics widget opened in the Service Portal Designer](../image/service-portal-pa-widget2.png "Performance Analytics widget")

## Security requirements for viewing widgets

Starting with Quebec, widgets follow indicator and breakdown access control lists \(ACLs\). Outside of ACLs, no roles are required for viewing widgets.

However, if you upgrade an instance from a version earlier than Quebec, by default the rules from before Quebec still apply. Indicator and breakdown ACLs are followed only in these areas:

-   List widgets follow indicator ACLs.
-   When viewing breakdowns, breakdown ACLs apply.

Furthermore, on an upgraded instance, the following widgets may require users to have the pa\_viewer role:

-   List widgets
-   Text widgets
-   The Breakdowns section of Workbench widgets

Upgraded instances cannot automatically follow the rules introduced in Quebec because of the variation in how ACLs are configured.

**Related topics**  


[bundle-platux.t_ConfigureAPage]

[Reports on Service Portal](../../reporting/concept/service-portal-reporting-widget.md#)

[Performance Analytics widgets](c_Widgets.md)

## Activate the Performance Analytics and Reporting - Service Portal Widgets plugin

You can activate the Performance Analytics and Reporting - Service Portal Widgets plugin \(com.snc.pa.sp.widget\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

### Before you begin

Role required: admin

### About this task

The Service Portal Widget plugin activates these related plugins if they are not already active.

<table id="table_jmj_5yb_k1b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Portal\[com.glide.service-portal\]

</td><td>

Core Service Portal functionality.

</td></tr></tbody>
</table>### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[bundle-platadm.list-of-plugins]

