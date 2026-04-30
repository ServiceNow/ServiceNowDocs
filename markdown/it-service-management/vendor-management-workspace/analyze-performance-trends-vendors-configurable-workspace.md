---
title: Compare your vendor characteristics with high-performing vendors in Vendor Management Workspace
description: Monitor the attributes that define your vendor performance and compare them with top-performing vendors.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing vendors using Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Compare your vendor characteristics with high-performing vendors in Vendor Management Workspace

Monitor the attributes that define your vendor performance and compare them with top-performing vendors.

## Before you begin

**Important:** You must install the Success Indicators \(com.snc.vendor.insights\) plugin separately from the ServiceNow Store. For more information, see [Activate Vendor Management Workspace](activate-vendor-management-configurable-workspace.md).

Role required: sn\_vlm.vendor\_manager

Vendor Success Indicators uses the chi-square test that compares two values to see if they’re statistically different from what is expected.

**Note:**

-   The comparisons depend on how well the density curve of the chi-square value is distributed between the vendor characteristics.
-   When the degree of freedom is 1, then the p-value that measures probability between your comparisons must be less than 0.05 to have a statistical significance.
-   Ideally, your comparison data must include at least 5 vendor records each that have values closer to the upper and lower thresholds.

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Workspace**.

2.  Select a vendor.

3.  Select the Success Indicators icon \( ![Success Indicators icon](../image/success-indicators-icon.png)\).

4.  Analyze the metrics for your vendors and compare them against top performers.![Vendor Success Indicators](../image/vendor-success-indicators.png)

    **Note:** Vendors must meet the following criteria for evaluating against top-performing vendors:

    -   Have a vendor KPI group assigned to them
    -   Have a valid vendor score
    Only vendors who have a vendor KPI group assigned to them and also have a valid vendor score will be used for evaluating against top-performing vendors.

    The preceding image shows an example of success indicators for the company Cloud MSP. The success indicators provide insight into the top five attributes across all vendors that contribute to high performance. These indicators are displayed in the order of their contribution to the performance ranking which is as follows:

    1.  Average Availability
    2.  Average SLA Achievement
    3.  Avg Perf Score of SO
    4.  Avg. Customer Satisfaction
    For numeric attributes, the interpretation of the value depends on the direction set for the indicator.

5.  Select **See more** to drill down into the data.

    The following image shows the drill down data for the Average Performance Score for Service Offerings.

    ![Average Availability Success Indicator](../image/top-performance-indicator.png)

<table id="table_jbn_jtl_nrb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vendor display name \[Example: Cloud MSP\]

</td><td>

Displays the score for the selected attribute. The **Rank** field shows the overall vendor ranking for the attribute.**Note:** If the score falls outside the range of ranked vendors, the ranking displays as unranked.

</td></tr><tr><td>

My Top Performing Vendor

</td><td>

For the selected attribute, displays the score for the attribute. It also displays the ranking of the highest performing vendor among all the vendors that you manage.

</td></tr><tr><td>

Top Performing Vendor

</td><td>

For the selected attribute, displays the score for the attribute. It also displays the ranking of the highest performing vendor among all vendors in your organization.

</td></tr></tbody>
</table>    |Name|Description|
    |----|-----------|
    |My Top Vendors|Displays the ranking and success indicator attribute details of all vendors that you manage.|
    |Top Vendors|Displays the ranking and success indicator attribute details of all vendors in your organization.|

    You can select a rank or the name of a vendor to view the vendor profile.


**Parent Topic:**[Managing vendors using Vendor Management Workspace](../concept/using-vendor-management-workspace.md)

