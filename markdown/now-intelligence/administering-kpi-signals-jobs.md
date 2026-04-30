---
title: KPI Signals automated detection jobs
description: The KPI Signals application includes jobs that detect signals automatically. These jobs run so responsible users can be notified of new signals without opening the application. The job for signals on formula indicators requires scheduling.Set the PA - KPI Signals - Formula Indicator Signals Calculation Job to run after all data detection jobs have run.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# KPI Signals automated detection jobs

The KPI Signals application includes jobs that detect signals automatically. These jobs run so responsible users can be notified of new signals without opening the application. The job for signals on formula indicators requires scheduling.

When you view an indicator in KPI Details and open the KPI Signals panel, that indicator is checked for signals. You therefore always have the most up-to-date signals. However, the KPI Signals application also has automated signal detection jobs. These jobs send notifications about signals to subscribed users without them having the application open.

For [automated indicators](../../performance-analytics/concept/performance-analytics-glossary.md#), these jobs run whenever a [data collection job](../../performance-analytics/concept/performance-analytics-glossary.md#) runs. The KPI Signals application checks all indicator and [breakdown element](../../performance-analytics/concept/performance-analytics-glossary.md#) combinations that it is active for. The data collection jobs are domain specific, so the signals are also domain specific.

The situation is different for [formula indicators](../../performance-analytics/concept/performance-analytics-glossary.md#). The formula in a formula indicator uses the scores of other indicators. These other indicators are referred to as [contributing indicators](../../performance-analytics/concept/performance-analytics-glossary.md#). The scores of these indicators can be collected in different data collection jobs. Bear in mind the KPI Signals calculation uses the most recently detected contributing indicator scores. The KPI Signals job should run after the scores of all the contributing indicators have been detected.

To help you ensure that formula indicators are checked for signals at the right time, the KPI Signals application comes with a scheduled job: PA - KPI Signals - Formula Indicator Signals Calculation Job. This job has a default setting to run every 8 hours, but you have the possibility to optimize this timing.

## Schedule the job to detect signals for formula indicators

Set the PA - KPI Signals - Formula Indicator Signals Calculation Job to run after all data detection jobs have run.

### Before you begin

Review the Performance Analytics data detection jobs. Determine a time after these jobs have run that signals should be detected for formula indicators.

**Note:** This procedure is optional. Modifying the job schedule can prevent lags between new scores and new signals on formula indicators. However, the default signal detection every 8 hours should not produce errors and may be sufficient for you.

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the list for jobs whose name contains `KPI Signals`.

3.  Open the PA - KPI Signals - Formula Indicator Signals Calculation Job.

4.  Modify the following fields to schedule the job:

<table id="table_lhw_wbc_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

Frequency you want the job to run. The choice of subsequent fields depends on your setting in this field.By default, the job runs **Periodically**.

</td></tr><tr><td>

Day

</td><td>

Day you want the scheduled job to run. If you selected **Weekly** in the **Run** field, this field displays the days of the week. If you selected **Monthly** in the **Run** field, this field displays the days of the month.

</td></tr><tr><td>

Time

</td><td>

Time you want the scheduled job to start.

</td></tr><tr><td>

Repeat Interval

</td><td>

Number of days and hours before the scheduled job runs again. This field appears when **Periodically** is selected from the **Run** list.By default, the job runs every 8 hours.

</td></tr><tr><td>

Starting

</td><td>

Date and time to start the periodic updates. This field appears when **Periodically** is selected from the **Run** list.

</td></tr></tbody>
</table>
