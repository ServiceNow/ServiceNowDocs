---
title: Define a calculated metric data source
description: Define dynamic metrics using formulas based on other metrics.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Define the data source, Set up the Data Context Engine, Customer success, Customer Success Management, Customer Success Management]
---

# Define a calculated metric data source

Define dynamic metrics using formulas based on other metrics.

## Before you begin

-   Role required: sn\_acct\_lc.customer\_success\_application\_admin
-   Configuration guidelines:
    -   Select at least one Context table that matches the Breakdown table.
    -   Configure calculated metrics with appropriate segment configurations and data sources. Include at least one active filter in each data source that matches the Breakdown table.
    -   Use one data source per calculation to avoid duplicate scores for a single product. When multiple data sources are necessary for the same metric, make segment conditions mutually exclusive.

## Procedure

1.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources** &gt; **Create New**.

2.  Enter a name for the data source and select **Calculated** from the Source drop down list.

3.  In the **Breakdown table** field, select the source table against which the score is to be calculated.

    For example, if you’re calculating the health score for an engagement, select the Engagement table here. If you’re calculating the product adoption score, select the Sold Products table here.

4.  In the **Target table** field, select the table where the calculated score is written.

    Select a **Target field** and **Query field** in the Target table. The calculated score is written into the records in the Target table that match the context specified in the Query field.

    For example: If you have configured the Product Adoption Score data source as follows:

    -   Data source: Product adoption
    -   Target table: Product Usage
    -   Target field: Adoption score
    -   Target query field: Sold product
    If the calculated score for Sold product SP1 is 90.0, then in the Product Usage table, the Adoption score for all SP1 records is set to 90.0.

5.  Select **Submit** to create this data source.

6.  Navigate to the **Contexts** related list.

7.  In the Context page, select the table for which this data source is applicable.

    **Note:** You can define multiple context tables for a single data source. At least one context table must be the same as the Data source and Context defined in the newly created data source.

8.  Navigate to the **Segments** related list.

9.  Select **New**.

10. Enter a name for the segment and specify the **Rank**.

    The Rank field is used to specify the priority of the Segment.

11. The Breakdown table as specified in the Data Source is displayed.

12. Select **Add Filter Condition** and specify one of more conditions.

    You can define multiple condition-based variations for a single metric.

13. Select **Submit**.

14. Navigate to the **Segment Configurations** related list and select **New**.

    Each Segment can have one ore more segment configurations. A Segment configuration is used to define how the metric data is derived in different contexts.

15. In the Segment Configuration page, enter the following details:

    -   Metric: Select a PA Indicator, External, or Calculated metric from the list.

        **Note:**

        -   You can’t select a metric that has already been defined for the parent Segment.
        -   Only published data sources are available for selection. If a published data source that is part of a segment configuration is later moved to a non-published state, you will see the following message:

            `This data source is referenced by at least one other published data source's segment configuration. Moving into non-published state may impact those references.`

            The calculated metric will not work as expected as the data source is no longer in a published state.

    -   Weight: The weight or percentage assigned to this metric in calculating the overall score. If you’re defining two or more data sources for the health definition, the total weight across all the data sources should be equal to 100. For example, for these data sources, you can specify the Weight as follows:
        -   Daily collection of CSAT: 40
        -   Weekly cases: 40
        -   Daily cases: 20
    -   Target: You can select:
        -   Maximize: The higher the target, the better the score.

            CSAT score: A higher value indicates a better score.

        -   Minimize: The lower the target, the better the score.

            Number of P1 cases: Fewer cases indicate a better performance.

    -   Direction: If multiple data records are returned for a data source, select how the aggregate score should be calculated:
        -   Average
        -   Sum
16. Select **Submit** to create this segment configuration.


## Example

To calculate the product adoption score for two or more products, you can configure your data source as follows:

-   Select **Sold Product** in the **Breakdown table** field.
-   Create a segment for Sold Product A and define segment configurations with the following values:
    -   Segment Configuration 1: Metric = NPS, Weight = 60%
    -   Segment Configuration 2: Metric = Clicks, Weight = 40%
-   Create a segment for Sold Product B and define segment configurations with the following values:
    -   Segment Configuration 1: Metric = CSAT, Weight = 50%
    -   Segment Configuration 2: Metric = Time Spent, Weight = 40%

## What to do next

After defining the segments and segment configurations, the next step is to configure the context engine mapper. See [Configure the Context Engine Mapper](../concept/account-lifecycle-define-context-engine-mapper.md) for details.

