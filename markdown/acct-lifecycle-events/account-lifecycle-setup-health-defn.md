---
title: Calculate the engagement health score
description: Use the Calculated metric data source to determine the health score of an engagement.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage engagements, Customer success, Configure, Customer Success Management]
---

# Calculate the engagement health score

Use the **Calculated** metric data source to determine the health score of an engagement.

## Before you begin

-   Role required: sn\_acct\_lc.customer\_success\_application\_admin

## About this task

If you’re upgrading from Customer Success Management 5.3.10 or earlier versions, you must run the `sn_acct_lc.MigrateHealthDataUtil().markHealthTablesDeprecated()` script to migrate data from the Engagement Health Definition and Health Metric Configuration tables to the **Calculated** metric data source. For more details, see [KB2668490](https://support.servicenow.com/kb?sys_kb_id=39f4e5cb47a9f250b6d8aa25126d43a0&id=kb_article_view).

## Procedure

1.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources** &gt; **Create New**.

2.  Enter a name for the data source and select **Calculated** from the Source drop down list.

3.  In the **Breakdown table** field, select the source table that is used to calculate the score.

4.  In the **Target table** field, select the table where the calculated score is written.

5.  Select a **Target field** and **Target Query field** in the Target table.

    The calculated score is written into the records in the Target table that match the context specified in the Query field. For calculating the health score of an engagement, you can configure the data source as follows:

    -   Breakdown table: Engagement
    -   Target table: Engagement
    -   Target field: Health score
    -   Target query field: sys\_id
6.  Select **Submit** to create the **Calculated** data source.

7.  Select **New** in the Segments related list.

8.  Enter a name for the segment and specify the **Rank**.

    The Rank field is used to specify the priority of the Segment. The Breakdown table as specified in the Data Source is displayed.

9.  Select **Add Filter Condition** and specify one of more conditions.

    You can define multiple condition-based variations for a single metric.

10. Select **Submit**.

11. Navigate to the Segment Configurations related list and select **New**.

12. Select **Submit** to create this segment configuration.

13. Enter the following details.

<table id="table_pcd_ndn_ydc"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

The **Calculated** data source that is used to determine the health score.

</td></tr><tr><td>

Target

</td><td>

This is the target or ideal health score for the engagement.

</td></tr><tr><td>

Weight

</td><td>

The weight or percentage assigned to this metric in calculating the overall health score of the engagement. If you’re defining two or more data sources for the health definition, the total weight across all the data sources should be equal to 100.For example, for these data sources, you can specify the Weight as follows:

-   Daily collection of CSAT: 40
-   Weekly cases: 40
-   Daily cases: 20


</td></tr><tr><td>

Direction

</td><td>

-   Maximize: The higher the target, the better the score. For example, CSAT score: A higher value indicates a better score.
-   Minimize: The lower the target, the better the score. For example, Number of P1 cases: Fewer cases indicates a better performance.


</td></tr><tr><td>

Aggregate

</td><td>

If multiple data records are returned for a data source, select how the aggregate score should be calculated:-   Average
-   Sum


</td></tr></tbody>
</table>14. Click **Submit** to create a new segment configuration.


## What to do next

Create a new visualization using the newly created data source. See [Configure DCE Visualizations](account-lifecycle-configure-dce-visual.md) for details. When the next data collection occurs, the health score is calculated and published on the Engagement page.

**Parent Topic:**[Manage engagements](../concept/account-lifecycle-manage-engagement.md)

