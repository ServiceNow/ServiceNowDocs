---
title: ITOM/OT SU Licensing dashboard
description: Use the ITOM Licensing dashboard to review the statistics of the resource consumption and status against your purchased subscriptions. This dashboard contains reports for each ITOM application. The reports offer visualization of the daily usage count and of the average consumption of subscription units for 90 days.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITOM/OT SU Licensing Reference, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# ITOM/OT SU Licensing dashboard

Use the ITOM Licensing dashboard to review the statistics of the resource consumption and status against your purchased subscriptions. This dashboard contains reports for each ITOM application. The reports offer visualization of the daily usage count and of the average consumption of subscription units for 90 days.

The ITOM Licensing dashboard is a part of ITOM Licensing application. See also OTM Licensing Dashboard at **All** &gt; **OTM** &gt; **** &gt; **OTM License** &gt; **OTM Licensing Dashboard**.

Role required: sn\_itom\_license.reader

## Access the Assessment dashboard

Ensure that you have an sn\_itom\_license.reader role to access the ITOM Licensing Dashboard located at **All** &gt; **ITOM License** &gt; **ITOM Licensing Dashboard**.

![ITOM Licensing Dashboard](../image/itom-licensing-dashboard-021126.png "ITOM Licensing dashboard") ![]( "ITOM Licensing dashboard")

## Use cases

As an example of how people in your organization would use this dashboard, see the following use case.

|User|Dashboard use|
|----|-------------|
|sn\_itom\_license.reader|Validate the resource usage for different ITOM products. Report the cases where the organization exceeded the number of purchased subscription units for specific resources.|

**Note:** ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

## Data visualization

The dashboard includes the following visualization:

<table id="table_lcd_5vt_yrb"><thead><tr><th>

Usage

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   ITOM Visibility
-   ITOM AIOps
-   Health Log Analytics
-   ITOM Cloud Accelerate
-   ITOM Discovery
-   ITOM Optimization
-   ITOM Digital End-User Experience \(DEX\)
-   ITOM Service Observability

</td><td>

§

</td><td>

ITOM Licensing CI Counts \[itom\_lu\_ci\_counts\] and UsageAnalytics Counts for Tables \[usageanalytics\_count\]

</td><td>

The first area displays the daily raw resource counts that include all the detected resources before sorting them into specific CIs. Hover over the bars to see the table of resource types. Each type is shown with an absolute number of resources and a share that it takes among others.

The second area displays bars that represent Subscription units counts for different licensable categories for the last 120 days per ITOM application. The dashboard also displays the brown line that represents the Usage Analytics counts table. This count is based on average consumption of subscription units for the last 90 days using SU ratios where one server, three PaaS resources, three containers, or one unresolved monitored object equal 1 SU.

Hover over the vertical bar in the Subscription units area for the desired day to open the Available CIs list. The table shows each CI category included in the daily CI count, along with the absolute number of resources and the share that it takes among others.

The third area shows which version of the ITOM Licensing is used on the instance each day. It helps explain spikes in count every time the new version is installed.

</td></tr></tbody>
</table>**Parent Topic:**[ITOM/OT SU Licensing Reference](../../../product/it-operations-management/reference/itom-su-licensing-reference.md)

