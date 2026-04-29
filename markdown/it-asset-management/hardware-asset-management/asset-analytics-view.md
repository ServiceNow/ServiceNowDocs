---
title: Asset analytics view
description: Use the Asset analytics view to get a detailed view of all your hardware assets, the total cost of ownership \(TCO\) of your assets, and the asset performance.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset analytics view

Use the Asset analytics view to get a detailed view of all your hardware assets, the total cost of ownership \(TCO\) of your assets, and the asset performance.

## Total cost of ownership

For more information about the TCO of your assets, see [Asset Total Cost of Ownership for Hardware Asset Management](asset-mgmt-tco.md).

**Important:** The Asset Analytics view is available with Hardware Asset Management 10.0.0 version or later.

![Asset analytics view in Hardware Asset Workspace.](../image/ham-asset-analytics.png)

You can filter and narrow down your results by selecting a location, stockroom, and model category.

**Note:**

TCO reports support domain separation when Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) and Domain Support \(com.snc.pa.domain\_support\) plugins are activated.

<table id="table_r31_5g2_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reached benchmark TCO

</td><td>

The number of assets that have their TCO more than or equal to the benchmark cost.

</td></tr><tr><td>

Approaching benchmark TCO

</td><td>

The number of assets that have their TCO more than or equal to the benchmark threshold but less than the benchmark cost.The TCO benchmark threshold percentage is set to 75% of the TCO benchmark cost by default.

For example, if you have set the benchmark as $1000 and the asset cost has reached $750, the asset is considered to be approaching the benchmark TCO.

Use the system property **sn\_itam\_common.asset\_tco\_benchmark\_threshold\_percentage** to update the benchmark threshold percentage.

For more information about the hardware asset field values, see [Asset record fields](../../asset-management/reference/asset-record-fields.md).

</td></tr><tr><td>

Capital planning

</td><td>

Number of assets for capital planning. The Assets for capital planning are assets that are not retired and their current life cycle phase is true.

</td></tr><tr><td>

Top 10 models with highest average TCO

</td><td>

Top 10 models that have the highest average asset TCO in a 12-month duration.

</td></tr><tr><td>

Asset reached benchmark cost by category

</td><td>

Number of assets whose asset TCO has reached benchmark cost based on model category.

</td></tr><tr><td>

Assets expense distribution

</td><td>

Costs incurred on your assets based on the expense categories such as labor, shipment, and purchase.

</td></tr><tr><td>

Monthly asset expense distribution \(last 12 months\)

</td><td>

Monthly initial and operational costs of your assets over the last 12 months.

</td></tr></tbody>
</table>-   **Comparative reports**

    View the most recently created TCO reports in this section.

    You can also create a report by selecting **New** in the Comparative reports section. For more information, [Create a TCO report in Hardware Asset Workspace](../task/create-ham-tco-report.md).


## Asset performance

The Asset performance tab provides details on the average values of the following key performance indicators \(KPIs\):

-   Availability
-   Mean time between failures \(MTBF\)
-   Mean time to repair \(MTTR\)

**Note:** For more details on calculation of KPIs, see [Asset performance reports in the Hardware Asset Workspace](asset-performance-reports-ham.md).

By default, the **Model category** filter is applied to the KPI reports. To further narrow down and focus on specific data, you can also select any one of the following filters:

-   **Domain**
-   **Location**
-   **Classification**
-   **Model**

**Note:** You can apply a maximum of two filters to any KPI report.

You can see a weekly trend of the average KPI values in the report. The Asset Availability list provides KPI details for all hardware assets that are tracked. The average KPI values are calculated based on the assets in this list.

When you select any KPI report, the **KPI Details** page appears. This page enables you to explore the information within that KPI. You can set targets you want to achieve and also set signals to notify you of any significant changes in the KPI.

![Asset performance tab in the Asset analytics view](../image/asset-performance-view-ham.png "Asset performance dashboard")

|Widget|Description|
|------|-----------|
|Availability|Average availability percentage of all hardware assets that are tracked, calculated by dividing the total asset availability percentage by the number of assets listed in the Asset availability report.|
|MTBF|Average MTBF of all hardware assets that are tracked, calculated by dividing the total Asset MTBF by the number of assets listed in the Asset availability report.|
|MTTR|Average MTTR of all hardware assets that are tracked, calculated by dividing the total Asset MTTR by the number of assets listed in the Asset availability report.|
|Asset availability|Report that lists the availability and other related KPIs of all hardware assets that are tracked.|

