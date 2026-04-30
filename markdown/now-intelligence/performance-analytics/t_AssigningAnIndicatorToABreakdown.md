---
title: Assign an indicator to an automated breakdown
description: Associate automated or formula indicators with a breakdown to enable the collection of broken down scores for those indicators.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated breakdowns, Performance Analytics breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Assign an indicator to an automated breakdown

Associate automated or formula indicators with a breakdown to enable the collection of broken down scores for those indicators.

## Before you begin

The breakdown must have a breakdown mapping for the indicator source table.

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Automated Breakdowns**.

2.  Select a breakdown record.

3.  In the **Indicators** related list, click **Edit**.

4.  Use the slushbucket to select the indicators you want to assign to this breakdown.

5.  Click **Save**.

6.  In the **Indicator Breakdowns** related list, set the **Display** value to false to hide the breakdown on the Analytics Hub and dashboard widgets.

    If the **Display** field is false, broken-down scores are still populated during data collection, but the breakdown is not selectable on the Analytics Hub or on dashboard widgets.


## What to do next

Run a data collection jobs on the indicator to collect scores for the new breakdown.

**Important:** If you add a breakdown to an existing indicator for which you already have scores, be careful to collect scores for the new breakdown without overwriting any collected scores.

For this purpose, create a special one-off collection job. Set the job to collect data for as far back as you need. Select only the indicator or indicators to which you have added this breakdown. Configure the resulting job indicators to exclude all other breakdowns. Clear the **Collect indicator** option on the job indicators. Then run the job.

If your role does not allow you to create collection jobs, contact your Performance Analytics admin.

For more information, see [Create or schedule a data collection job](t_CreatASchedDataCollJob.md) and [Configure a job indicator](configure-job-indicator.md).

**Parent Topic:**[Automated breakdowns](../concept/automated-breakdowns.md)

**Previous topic:**[Create a breakdown mapping on a breakdown record](t_CrtBkdnBreakdownMpngs.md)

**Next topic:**[Manual breakdowns](../concept/manual-breakdowns.md#)

