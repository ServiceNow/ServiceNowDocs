---
title: Configure DCE Visualizations
description: Use the DCE Visualizations option to configure data sources, define baselines and targets, and apply aggregation rules. You can also define specific conditions to customize the data displayed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Data Context Engine, Customer success, Configure, Customer Success Management]
---

# Configure DCE Visualizations

Use the DCE Visualizations option to configure data sources, define baselines and targets, and apply aggregation rules. You can also define specific conditions to customize the data displayed.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_application\_admin

## Procedure

1.  Navigate to **All** &gt; **Data Context Engine** &gt; **Insights** &gt; **All DCE Visualizations**.

2.  Select **New**.

3.  Enter the following details on the form.

<table id="table_kms_zmz_vfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Select the data source that will be used to collect the data for visualization.

</td></tr><tr><td>

Resolving Context

</td><td>

Select the context table on which the visualization is to be applied. For usage data such as adoption score or satisfaction score, select the Sold Products table.

</td></tr><tr><td>

Conditions

</td><td>

Define additional conditions to customize how the data is displayed.

</td></tr><tr><td>

Baseline

</td><td>

Specify the standard or expected value for this metric.

</td></tr><tr><td>

Target

</td><td>

Specify the target or desired goal for this metric.

</td></tr><tr><td>

Aggregate

</td><td>

If multiple data records are returned for a data source, select how the aggregate score should be calculated:-   Average
-   Sum


</td></tr><tr><td>

Direction

</td><td>

You can select:-   Maximize: The higher the target, the better the score. For example, CSAT score: A higher value indicates a better score.
-   Minimize: The lower the target, the better the score. For example, Number of P1 cases: Fewer cases indicates a better performance.


</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Navigate to the DCE Visualizations M2Ms Related list and select **New**.

6.  Select a **DCE Insights Item** from the list.

    The DCE Insights Item maps a specific visualization to a designated location on a layout, ensuring that insights are displayed in the right context within the user interface. The DCE Insights Item table contains the following fields.

7.  Specify the Rank for this visualization and select **Submit**.

    Navigate to [View product usage and capability data](../concept/account-lifecycle-prod-cap-usage.md) to view the configured metrics.

    **Note:** You can use the [Color banding table](account-lifecycle-setup-color-banding.md) to configure the colors that appear on the charts that appear on the product usage and capability pages.


