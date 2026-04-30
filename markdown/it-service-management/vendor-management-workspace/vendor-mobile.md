---
title: ITSM Vendor Management Mobile dashboard
description: Analyze vendors by KPI group. You can see which contracts were created in the last 30 days and which ones are ending in the next 90 days. Monitor improvement initiatives for your vendors.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ITSM Vendor Management Mobile for Vendor Management Workspace, Managing vendors using Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# ITSM Vendor Management Mobile dashboard

Analyze vendors by KPI group. You can see which contracts were created in the last 30 days and which ones are ending in the next 90 days. Monitor improvement initiatives for your vendors.

![Vendor Management Mobile](../../../product/vendor-management-workspace/image/vendor-management-mobile.jpg)

## Required Vendor Management Mobile roles

If you have the Vendor Manager \[sn\_vlm.vendor\_manager\] role, you can access the Vendor Management Mobile landing page.

## Use cases

<table id="table_uj4_rww_r4b"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

As a vendor manager, you can analyze real-time details such as:-   Breakdown of vendors by KPI groups.
-   How many new contracts were created in the last 30 days.
-   How many contracts are ending in the next 90 days.
-   Analyze improvement initiatives for your vendors.

</td><td>

Vendor Manager \[sn\_vlm.vendor\_manager\]

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Vendors by KPI group|Donut![Donut](../../reporting/image/icon-donut-report.png)|Company \[core\_company\]|Breakdown of vendors by metric model.|
|New contracts|Single score![Single score report](../../performance-analytics/image/single-score.png)|Contract \[ast\_contract\]|Number of contracts created in the last 30 days.|
|Contracts ending|Single score![Single score report](../../performance-analytics/image/single-score.png)|Contract \[ast\_contract\]|Number of contracts ending the next 90 days.|
|Improvement initiatives|Single score![Single score report](../../performance-analytics/image/single-score.png)|Improvement Initiative \[sn\_cim\_register\]|Number of improvement initiatives created for your vendors.|

## Lists

Access the following vendor lists on the Vendor Management Mobile dashboard.

|Name|Description|
|----|-----------|
|My Vendors|List of all vendors managed by the vendor manager.|
|All Vendors|List of all vendors in your organization.|
|My Vendor Incidents|List of all incidents monitored by the vendor manager.|
|My Vendor Outages|List of all outages monitored by the vendor manager.|
|My Vendors Breached SLA|List of breached SLAs monitored by the vendor manager.|

**Parent Topic:**[ITSM Vendor Management Mobile for Vendor Management Workspace](../../../product/vendor-management-workspace/concept/vendor-mobile-vendor-management-workspace.md)

