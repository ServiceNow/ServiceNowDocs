---
title: Add a collection job to an indicator
description: To collect scores for an automated indicator, add a collection job to that indicator.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add a collection job to an indicator

To collect scores for an automated indicator, add a collection job to that indicator.

## Before you begin

**Note:** This procedure shows how to add fully configured data collection jobs to an automated indicator, from the indicator side. For information about configuring data collection jobs and adding them to indicators from the job side, see [Configure a job indicator](configure-job-indicator.md). Only persons with the pa\_data\_collector role, such as Performance Analytics administrators, can configure job indicators.

Role required: pa\_power\_user, or admin

## Procedure

1.  Open an existing automated indicator.

2.  In the **Jobs** related list, click **Edit**.

    ![The Jobs related list in an automated indicator record](../image/auto-ind-jobs-rl.png)

3.  Use **Add Filter** and **Run Filter** to limit the selection of jobs.

4.  Select one or more jobs in the **Collections** or **Jobs List**.

    Unless you have a clear use case to do otherwise, help keep your jobs manageable by selecting no more than one scheduled job for your indicator. Select as many unscheduled jobs as are relevant. Generally, add one historical job that you run only once on a new indicator.

5.  Use the arrow buttons to move the jobs to the other list.

6.  Click **Save**.


**Parent Topic:**[Automated indicators](../concept/automated-indicators.md)

**Previous topic:**[Assign and map breakdowns](create-breakdown-mapping.md#)

**Next topic:**[Performance Analytics snapshots](../concept/pa-snapshots.md)

