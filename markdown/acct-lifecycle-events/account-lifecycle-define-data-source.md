---
title: Define the data source
description: Before the health or risk score can be calculated, you must specify the source from which data is to be collected. Data can be collected either through key performance metrics or external sources.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setup the data context engine, Configure customer success, Customer success, Customer Success Management]
---

# Define the data source

Before the health or risk score can be calculated, you must specify the source from which data is to be collected. Data can be collected either through key performance metrics or external sources.

To define the data source, follow these steps:

1.  Login as a user with the `sn_acct_lc.ale_success_agent` role.
2.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources** &gt; **Create New**.
3.  Enter the following details:

<table id="table_gtm_2sk_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the data source.

</td></tr><tr><td>

Source

</td><td>

Select the source from which the data is to be collected. This can be:-   PA indicator: An automated scheduled job collects data and creates records in the Context Engine Data table.
-   External: Specify the external data source from which the data is to be collected.
**Note:** If you select the **External** option, you must define how this data can be retrieved from the external source or use the [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) to save this information in the Context Engine data table.

</td></tr><tr><td>

Frequency

</td><td>

Select the frequency at which the data should be collected. This can be:-   Daily
-   Weekly
-   Monthly
-   Quarterly
**Note:** If you select PA Indicator as your data source, you must select a frequency equal to or greater than the PA Indicator collection frequency. For example, if the PA Indicator is collecting data once a week, you cannot select a frequency that is lower than Weekly here.

</td></tr><tr><td>

PA indicator

</td><td>

Select the metric for which the data is being collected.

</td></tr><tr><td>

Breakdown

</td><td>

Select the attribute or category by which the health or risk score is to be grouped. This can be account, product, and so on.

</td></tr><tr><td>

Unit of measurement

</td><td>

Select the unit of measurement for the PA indicator. This can be minutes, hours, days, months, and so on.

</td></tr><tr><td>

Aggregate

</td><td>

Select how the aggregate score should be calculated. This can be:-   Average
-   Sum
-   Max
-   Min
The Aggregate score is useful if you select a Frequency that is different from the collection frequency of the PA indicator. For example, suppose the PA indicator collection frequency is set to Daily, and the Frequency is set to Weekly, you need to calculate the aggregate score for the week. In this case, you can use the average or sum option to calculate the score.

</td></tr></tbody>
</table>4.  Click **Submit** to create this data source.
5.  Navigate to the Contexts related list and click **New**.
6.  In the Context page, select the table for which this data source is applicable. This can be an engagement or success outcome table. You can define multiple context tables for a single data source.

    **Note:**

    -   For calculating the health score, you must select the Engagement table.
    -   For calculating the success outcome, you must select the Success Outcome table.
7.  Enable the **Active** checkbox and click **Submit** to create the data source. You can associate the data source with one or more context tables.

After setting up the data source and the context, you set up the context engine mapper.

