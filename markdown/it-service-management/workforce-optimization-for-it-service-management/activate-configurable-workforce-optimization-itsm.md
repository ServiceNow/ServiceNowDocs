---
title: Activate Workforce Optimization for ITSM
description: The Workforce Optimization for ITSM Configurable Workspace plugin \(sn\_wfo\_cfg\_itsm\) is available with the ITSM Enterprise subscription package.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Getting started, Workforce Optimization for ITSM, IT Service Management]
---

# Activate Workforce Optimization for ITSM

The Workforce Optimization for ITSM Configurable Workspace plugin \(sn\_wfo\_cfg\_itsm\) is available with the ITSM Enterprise subscription package.

## Before you begin

Role required: admin

## About this task

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

<table id="table_vgp_3dq_n4b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workforce Optimization for ITSM Configurable Workspace \(sn\_wfo\_cfg\_itsm\) **Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates related plugins that enable you to use the Scheduling, Work Scheduler, Coaching, Teams, and Channel Management applications in Workforce Optimization for ITSM.

</td></tr><tr><td>

MetricBase \(com.snc.clotho\)

</td><td>

Enables you to use Demand Forecast in Workforce Optimization for ITSM.To use Demand Forecast, you must activate the MetricBase plugin before you activate the Workforce Optimization for ITSM plugin. For more information, see [Request the MetricBase product](https://www.servicenow.com/docs/access?context=request-metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

 When you activate both of these plugins, the Agent Forecast plugin \(com.sn\_agent\_forecast\) is activated.

</td></tr><tr><td>

ITSM Virtual Agent Conversations\(com.snc.itsm.virtualagent\)

 **Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates the ITSM Virtual Agent and enables you to use a virtual agent to create time-off requests.

</td></tr><tr><td>

ITSM Mobile Agent for Workforce Optimization for ITSM **Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activates the ITSM Mobile Agent and enables agents to request shift-swaps or time off and managers to approve the requests using the ITSM Mobile Agent application.

</td></tr><tr><td>

Process Mining plugin \(com.sn\_po\).

</td><td>

Integrates Process Mining with Workforce Optimization for ITSM.

</td></tr></tbody>
</table>You can also get these Workforce Optimization for ITSM application plugins from the ServiceNow Store.

<table id="table_ryb_5nz_31c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team Performance \(sn\_team\_perf\)

 **Note:** When you install this plugin, make sure that you’ve upgraded the following plugins to the latest store release version:

-   Workforce Optimization for ITSM Configurable Workspace \(sn\_wfo\_cfg\_itsm\).
-   Workforce Optimization Configurable Workspace Core \(sn\_wfo\_cfg\_ws\).
-   Workforce Optimization Common\(sn\_wfo\_common\).

</td><td>

Enables you to track and analyze performance trends for your teams from a single location.

**Important:** This plugin gets automatically installed when the Workforce Optimization for ITSM Configurable Workspace \(sn\_wfo\_cfg\_itsm\) plugin is activated.

</td></tr><tr><td>

Coaching \(sn\_coaching\)

 **Note:** When you install the Coaching \(sn\_coaching\) plugin, make sure that you’ve upgraded the following plugins to the latest store release version:

-   Workforce Optimization for ITSM Configurable Workspace \(sn\_wfo\_cfg\_itsm\).
-   Workforce Optimization Configurable Workspace Core \(sn\_wfo\_cfg\_ws\).
-   Workforce Optimization Common \(sn\_wfo\_common\).

</td><td>

Enables you to assess your teams' abilities to resolve incidents efficiently.

**Important:** This plugin gets automatically installed when the Workforce Optimization for ITSM Configurable Workspace \(sn\_wfo\_cfg\_itsm\) plugin is activated.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Getting started with Workforce Optimization for ITSM](../concept/getting-started-workforce-optimization-itsm.md)

