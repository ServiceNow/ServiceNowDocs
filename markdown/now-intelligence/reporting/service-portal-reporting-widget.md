---
title: Reports on Service Portal
description: Show existing reports in a Service Portal.You can activate the Performance Analytics and Reporting - Service Portal Widgets plugin \(com.snc.pa.sp.widget\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Reports on Service Portal

Show existing reports in a Service Portal.

When you edit a portal, add the **Report** widget. Use the widget options to specify a report to show on the service portal and whether to show the title of the report. The widget lists created in the Report Designer. For more information, see [Create a report](../task/t_CreateYourOwnReport.md#).

![Report widget opened in the Service Portal Designer](../image/service-portal-report-widget2.png "Report widget")

With the report widget, you can show all report types on your portal except for list reports. Use the [Simple List Widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/simple-list-widget.md) instead.

**Parent Topic:**[Using reporting](c_GenerateReports.md)

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


[List of plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

