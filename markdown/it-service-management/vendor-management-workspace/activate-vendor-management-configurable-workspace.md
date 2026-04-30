---
title: Activate Vendor Management Workspace
description: The Vendor Manager Workspace \(sn\_itsm\_vendor\) plugin is available with the ITSM Pro subscription package. This plugin activates related plugins if they are not already active.
locale: en-US
release: xanadu
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Activate Vendor Management Workspace

The Vendor Manager Workspace \(sn\_itsm\_vendor\) plugin is available with the ITSM Pro subscription package. This plugin activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

<table id="table_q5j_gny_ngb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor Manager Workspace \(sn\_itsm\_vendor\)**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates the Performance Analytics Premium for Service Management \(com.snc.pa.premium.service\_management\) plugin that adds the following functionality to Vendor Management Workspace:

-   Create indicators, breakdowns, and other records.
-   Create text analytics widgets.
-   Use Performance Analytics with external data.
-   Preserve performance scores beyond 180 days.

 Activates the Continual Improvement Management \(com.sn\_cim\) plugin. This plugin enables you to monitor the continual improvement initiatives that your vendors are engaged with.

</td></tr><tr><td>

Vendor Success Indicators \(com.snc.vendor.insights\)**Important:** This plugin is being planned for deprecation after August 1, 2024. It will be hidden and no longer available for activation for new customers but will continue to work and be supported for existing customers. For details, see the [Deprecation process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184).

</td><td>

Activates success indicators and adds the following functionality to gain insights into how your vendors are performing in comparison with other vendors in your organization.

</td></tr><tr><td>

Vendor Management Mobile \(sn\_vendor\_mobile\)**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates the Vendor Mobile Agent app

</td></tr></tbody>
</table>You can also integrate Vendor Management Workspace with the Vendor Risk Management application when you enable the Vendor Risk Management \(app-vendor-risk-management\) plugin.

If you have downloaded the Vendor Risk Management application that is available from the ServiceNow Store, you can view the risk rating for your vendors. For more information on downloading the Vendor Risk Management application, refer to [Download a GRC application from the ServiceNow Store for the first time](https://www.servicenow.com/docs/access?context=download-grc-first-time&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

When you enable the GRC: Vendor Risk Management Workspace \(sn\_vrm\_ws\) plugin from the ServiceNow Store you can view Vendor Risk Workspace within the Vendor Management Workspace application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


