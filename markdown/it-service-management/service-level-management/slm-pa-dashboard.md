---
title: Service level management PA dashboard
description: The Service Level Agreement \(SLA\) Overview module provides a Performance Analytics \(PA\) Dashboard to review SLA information at a glance.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Legacy: Platform Analytics Solutions for Service Level Management, Service Level Management reference, Service Level Management, IT Service Management]
---

# Service level management PA dashboard

The Service Level Agreement \(SLA\) Overview module provides a Performance Analytics \(PA\) Dashboard to review SLA information at a glance.

Users with the itil role can access the dashboard.

You can navigate to the PA dashboard in the following ways:

-   **Service Level Management** &gt; **Overview**
-   **Self – Service** &gt; **Dashboard** &gt; **SLA Overview \(Premium\)**

This dashboard has the following requirements:

-   An entitlement to use Performance Analytics with Service Level Management.
-   The Service Level Management PA Dashboard \(com.snc.pa.sla.overview\) plugin, which contains this dashboard.
-   The SLA Breakdowns plugin \(com.snc.sla.breakdowns\) plugin, because some of the reports are generated from the breakdown data.

## Overview tab

![sla pa dashboard](../image/sla-pa-dashboard1.png "SLA PA dashboard - Overview")

<table id="table_ksk_bkk_zdb"><thead><tr><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration of Active Breached SLAs

</td><td>

Uses available SLA breakdown data to generate a report showing time spent working on breached task SLAs that are still active and the SLA Definition Type is SLA.

 Use the Group by and Stacked By breakdown lists to show different representations of this data, for example: Group by Assignment group and Stacked By SLA Definition.

 The Assignment Group filter on the right can be used to limit the data shown in this report to a specific group.

</td></tr><tr><td>

Active Breached SLAs

</td><td>

This chart shows all breached task SLAs that are still active and the SLA Definition Type is SLA.

 Use the Group by and Stacked By breakdown lists to show different representations of this data, for example: Group by Assignment group and Stacked By SLA Definition.

 The Assignment Group filter on the right can be used to limit the data shown in this report to a specific group.

</td></tr><tr><td>

Achieved SLAs in Last 30 Days

</td><td>

This chart shows all task SLAs that completed in the last 30 days without breaching and where the SLA Definition Type is SLA.

 Use the Group by and Stacked By breakdown lists to show different representations of this data, for example: Group by Assignment group and Stacked By SLA Definition.

</td></tr></tbody>
</table>## KPI tab

The KPI dashboard uses the following Performance Analytics indicators:

|Indicator|Version introduced|
|---------|------------------|
|Average durations of breached task SLA closed today|London|
|Number of closed task SLA today|London|
|Average duration of achieved SLA today|London|
|Number of achieved closed task SLA today|London|
|Achieved SLAs Today|London|

**Note:** These indicators are calculated on a daily basis to provide trend analysis.

Further operations are performed on the Performance Analytics indicators to generate the following KPIs on the dashboard:

<table id="table_hnc_kwg_zdb"><thead><tr><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of Active Breached SLAs \(Daily\)

</td><td>

Shows the % of active task SLAs that breached yesterday.

</td></tr><tr><td>

Average Assignment Duration \(Breached\)

</td><td>

Shows the average duration of individual assignments for breached task SLAs completed yesterday. The KPI that provides the data captures this value on a daily basis to provide trend analysis.

 This report is based on SLA breakdown data and so shows data only for SLA definitions that are linked to an [SLA Breakdown definition](sla-breakdown-definition.md).

</td></tr><tr><td>

% of Achieved SLAs \(Daily\)

</td><td>

Shows the % of task SLAs that were completed yesterday without breaching. The KPI that provides the data captures this value on a daily basis to provide trend analysis.

</td></tr><tr><td>

Average Assignment Duration \(Achieved\)

</td><td>

Shows the average duration of individual assignments for achieved task SLAs completed yesterday. The KPI that provides the data captures this value on a daily basis to provide trend analysis.

 This report is based on SLA breakdown data and shows data only for SLA definitions that are linked to an [SLA Breakdown definition](sla-breakdown-definition.md).

</td></tr><tr><td>

Average Duration of Assignments for Breached SLAs

</td><td>

Shows the average duration of individual assignments for breached task SLAs completed yesterday broken down by either Assignment group or SLA Definition. Use the **Breakdown** field to change which breakdown data is displayed.

 The KPI that provides the data captures this value on a daily basis to provide trend analysis.

 This report is based on SLA breakdown data and shows data only for SLA definitions that are linked to an [SLA Breakdown definition](sla-breakdown-definition.md).

</td></tr><tr><td>

Average Duration of Assignments for Achieved SLAs

</td><td>

Shows the average duration of individual assignments for achieved task SLAs completed yesterday broken down by either Assignment group or SLA Definition. Use the **Breakdown** field to change which breakdown data is displayed.

 The KPI that provides the data captures this value on a daily basis to provide trend analysis.

 This report is based on SLA Breakdown data and shows data only for SLA definitions that are linked to an [SLA Breakdown definition](sla-breakdown-definition.md).

</td></tr></tbody>
</table>**Parent Topic:**[Legacy: Platform Analytics Solutions for Service Level Management](../../../use/dashboards/application-content-packs/service-level-mgmt-content-pack.md)

