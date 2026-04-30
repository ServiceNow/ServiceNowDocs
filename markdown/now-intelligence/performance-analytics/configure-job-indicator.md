---
title: Configure a job indicator
description: Increase the efficiency of data collection by configuring job indicators to collect only necessary and sensible data.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Collecting indicator scores, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Configure a job indicator

Increase the efficiency of data collection by configuring job indicators to collect only necessary and sensible data.

## Before you begin

Role required: admin, pa\_admin

## About this task

By default, a job indicator collects data for the indicator itself and for all breakdowns that are associated with that indicator. However, not all breakdown data might make sense for a particular [data collection job](../concept/performance-analytics-glossary.md#). For example, breakdowns that are based on fields that are likely to change over a collection period, such as Assignment Group and State, are usually excluded from historical jobs. Often, the job collects the value of Assignment Group and of State only at the time the job is run. A six-month-old incident, hopefully completed, can end up with a State of Complete for its entire six-month history. Such values are misleading.

Alternatively, you might need to collect only breakdown data and not to calculate the indicator scores. You can configure a job indicator not to collect unnecessary or meaningless data, thus reducing the resource consumption of the job.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Jobs**.

2.  Open the job for which you want to configure a job indicator.

    Job indicators are specific to the job that uses them.

3.  In the **Indicators** tab, click the name of the job indicator that you want to configure.

4.  Fill in the fields, as appropriate.

<table id="tbl_PerformanceAnalyticsDataCollectionJobIndicatorProperties"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Job

</td><td>

Is automatically copied from the job name.

</td></tr><tr><td>

Indicator

</td><td>

The associated automated indicator. When you add a job indicator with the **Edit** button on the Scheduled Data Collection record, you select the automated indicator.

</td></tr><tr><td>

Collect

</td><td>

Choose to collect **All breakdowns** or **No breakdowns**, or to exclude specific breakdowns.

</td></tr><tr><td>

Collect indicator

</td><td>

Select the check box to collect data for the indicator itself \(the default\). Clear this check box if you want to collect data for breakdowns alone. **Tip:** When you have added a breakdown to existing indicators, consider running a one-time historical collection job on these indicators to get scores for that breakdown. Collect only on the added breakdown and not for the indicators themselves.

</td></tr></tbody>
</table>5.  If in the **Collect** field you chose to **Exclude these breakdowns**, select breakdowns to exclude.

    1.  Open the context menu and click **Save**.

        A related list of excluded breakdowns appears.

    2.  Click **Edit** in the **Excluded breakdowns** list and add or remove breakdowns to exclude.


**Parent Topic:**[Collecting indicator scores](../concept/c_ClctData.md)

