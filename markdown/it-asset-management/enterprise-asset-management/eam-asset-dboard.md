---
title: Asset analytics overview for Enterprise Asset workspace
description: Use the Asset Analytics view to get a detailed view of all your assets, their overall performance, and the asset total cost of ownership \(TCO\).
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Enterprise Asset Workspace, Explore, Enterprise Asset Management, IT Asset Management]
---

# Asset analytics overview for Enterprise Asset workspace

Use the Asset Analytics view to get a detailed view of all your assets, their overall performance, and the asset total cost of ownership \(TCO\).

## Enterprise Asset Dashboard

Use the Enterprise Asset Dashboard to get comprehensive information on all your enterprise assets.

You can filter the data based on location, stockroom, model category, and classification.

![Enterprise Asset Dashboard](../image/asset-analytics-eam.png)

|Widget|Description|
|------|-----------|
|Asset count by model category|Number of assets grouped by the model category such as Medical General, Medical Diagnostic.|
|Asset count by lifecycle state|Number of assets grouped by the lifecycle state such as Retired, In use, and In stock.|
|Asset value by model category|Cost of assets grouped by the model category such as Vehicle, Cameras, and Field Devices.|

|Widget|Description|
|------|-----------|
|Model lifecycle overview|Overview of the model lifecycle grouped by the lifecycle phase such as **General Availability**, **End of Life**, **End of Support**, and **End of Sale**.|
|Discovered and undiscovered asset count|Comparison of the number of discovered and undiscovered assets grouped by model category.|
|Assets available for refresh by model category|Number of assets that have already expired or the current day is the expiry date, and are eligible for a refresh.|

## Asset TCO

This tab provides a detailed view of the TCO and displays key metrics that show the real-time status of assets regarding TCO benchmarks.

You can create new comparative reports and view existing ones.

You can filter the data based on location, stockroom, model category, and classification.

Select **View all** to view a list of all the comparative reports. Only reports that have at least one active report source are displayed with the exception of an offline report \(where the cost type is either **Actual TCO** or **Projected TCO**\). To update data sources on an offline report, open the report and select **Run update job**. This button only appears on an offline report. Once this job is complete, the latest collection date gets updated.

**Note:** Offline reports will not appear in the list of comparative reports until the latest collection date is populated.

You can select **New** to create a TCO report.

Select a report icon to directly open a report or select the report name to open the report form.

![Asset total cost of ownership](../image/asset-tco-tab.png)

<table id="table_gq4_323_jzb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reached benchmark TCO

</td><td>

Number of assets that reached the benchmark TCO.

</td></tr><tr><td>

Approaching benchmark TCO

</td><td>

Number of assets that are approaching the benchmark TCO

</td></tr><tr><td>

Capital planning

</td><td>

Number of assets for capital planning. The Assets for capital planning are assets that are not retired and their current life cycle phase is true.

</td></tr><tr><td>

Top 10 models with highest average TCO

</td><td>

A bar chart showing the top 10 models with the highest average TCO.

</td></tr><tr><td>

Assets reached benchmark cost by category

</td><td>

Number of assets by category that reached the benchmark cost.

</td></tr><tr><td>

Assets expense distribution

</td><td>

The asset expense distribution based on the following cost types:-   Purchase - Asset
-   Purchase - Part
-   Configuration
-   Software
-   Contract - Lease
-   Contract - Warranty
-   Contract - Maintenance
-   Contract - Service
-   Contract - Other
-   Utilities
-   Shipment
-   Labor - Maintenance
-   Labor - Repair
-   Labor - General
-   Resold value

</td></tr><tr><td>

Monthly asset expense distribution \(last 12 months\)

</td><td>

Distribution of assets over the last 12 months, based on the following cost types:-   Purchase - Asset
-   Purchase - Part
-   Configuration
-   Software
-   Contract - Lease
-   Contract - Warranty
-   Contract - Maintenance
-   Contract - Service
-   Contract - Other
-   Utilities
-   Shipment
-   Labor - Maintenance
-   Labor - Repair
-   Labor - General
-   Resold value

</td></tr></tbody>
</table>## Asset performance

The Asset performance tab provides details on the average values of the following key performance indicators \(KPIs\):

-   Availability
-   Mean time between failures \(MTBF\)
-   Mean time to repair \(MTTR\)

**Note:** For more details on calculation of KPIs, see [Asset performance reports in the Enterprise Asset Workspace](asset-performance-reports-eam.md).

By default, the **Model category** filter is applied to the KPI reports. To further narrow down and focus on specific data, you can also select any one of the following filters:

-   **Domain**
-   **Location**
-   **Classification**
-   **Model**

**Note:** You can apply a maximum of two filters to any KPI report.

You can see a weekly trend of the average KPI values in the report. The Asset Availability list provides KPI details for all enterprise assets that are tracked. The average KPI values are calculated based on the assets in this list.

When you select any KPI report, the **KPI Details** page appears. This page enables you to explore the information within that KPI. You can set targets you want to achieve and also set signals to notify you of any significant changes in the KPI.

![Asset performance tab in the Asset analytics view](../image/asset-performance-view-eam.png "Asset performance dashboard")

|Widget|Description|
|------|-----------|
|Availability|Average availability percentage of all enterprise assets that are tracked, calculated by dividing the total asset availability percentage by the number of assets listed in the Asset availability report.|
|MTBF|Average MTBF of all enterprise assets that are tracked, calculated by dividing the total Asset MTBF by the number of assets listed in the Asset availability report.|
|MTTR|Average MTTR of all enterprise assets that are tracked, calculated by dividing the total Asset MTTR by the number of assets listed in the Asset availability report.|
|Asset availability|Report that lists the availability and other related KPIs of all enterprise assets that are tracked.|

## Data Visualizations

The Data Visualizations tab enables the asset managers to view and create data visualizations in the Visualization Designer. As an asset manager, you can view the visualizations that are bookmarked, certified, owned by you, and shared with you. You can only edit the visualizations that you created.

![Data visualization report](../image/data-visualizations-eam.png "Data Visualizations tab")

