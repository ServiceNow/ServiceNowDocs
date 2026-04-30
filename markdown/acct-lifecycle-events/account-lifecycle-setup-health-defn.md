---
title: Setup the engagement health definition
description: Use the engagement health definition to configure the metrics required to calculate the health score for an engagement.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Setup the engagement health definition

Use the engagement health definition to configure the metrics required to calculate the health score for an engagement.

## Before you begin

-   Role required: sn\_acct\_lc.ale\_success\_agent
-   Data source and data context engine mapping must be setup. See [Setup the data context engine](../concept/account-lifecycle-setup-metric-data.md).

## About this task

To view the health scores for an engagement, you must setup the health definition and configure the health metrics. For each health definition, you can add one or more data sources that will be used to calculate the health score.

## Procedure

1.  Navigate to **All** &gt; **Success Configuration** &gt; **All Health Definitions** &gt; **New**.

2.  Enter the Name, Rank, and Description for the engagement.

    The Rank field is used to prioritize the health definition. The h

3.  Select the `Global configuration` checkbox if you want to apply this health definition to all engagements.

4.  If you want to apply the health definition to a specific engagement, add a filter condition in the Definition section.

    You can click on the `No of records matching the condition` link to view all engagements that match the condition.

    **Note:** Health definitions that are applicable to one or more engagements take precedence over the global health definition.

5.  Click **Submit** to create the health definition.

6.  Open the health definition you have created, navigate to the Health Metric Configurations related list, and click **New**.

    You can specify the data sources that will be used to calculate the health score of the engagement.

7.  Enter the following details:

<table id="table_pcd_ndn_ydc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Select the data source that will be used to calculate the health score.

</td></tr><tr><td>

Engagement health definition

</td><td>

The engagement for which this health metric is being configured.

</td></tr><tr><td>

Target

</td><td>

This is the target or ideal health score for the engagement.

</td></tr><tr><td>

Weight

</td><td>

The weight or percentage assigned to this metric in calculating the overall health score of the engagement. If you are defining two or more data sources for the health definition, the total weight across all the data sources should be equal to 100.For example, for these data sources, you can specify the Weight as follows:

-   Daily collection of CSAT: 40
-   Weekly cases: 40
-   Daily cases: 20


</td></tr><tr><td>

Direction

</td><td>

You can select:-   Maximize: The higher the target, the better the score.

For example, CSAT score: A higher value indicates a better score.

-   Minimize: The lower the target, the better the score.

For example, Number of P1 cases: Fewer cases indicates a better performance.

</td></tr><tr><td>

Aggregate

</td><td>

If multiple data records are returned for a data source, select how the aggregate score should be calculated:-   Average
-   Sum


</td></tr></tbody>
</table>8.  Click **Publish**.

    When the next data collection occurs, the health score is calculated and published on the Engagement page.


