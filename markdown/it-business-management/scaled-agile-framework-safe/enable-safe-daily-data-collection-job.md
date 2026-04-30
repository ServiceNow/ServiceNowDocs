---
title: Enable daily data collection for Essential SAFe dashboards
description: Enable scheduled data collection to begin collecting scores on new data automatically for Essential SAFe dashboards. Data collection jobs automatically collect scores for automated indicators and breakdowns.
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Enable daily data collection for Essential SAFe dashboards

Enable scheduled data collection to begin collecting scores on new data automatically for Essential SAFe dashboards. Data collection jobs automatically collect scores for automated indicators and breakdowns.

## Before you begin

Role required: pa\_admin or admin

## About this task

**Note:** Historical data collection is not supported for the underlying indicators of the \[SAFe\] Daily Data Collection job.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Find and open the \[SAFe\] Daily Data Collection job.

3.  Start the \[SAFe\] Daily Data Collection job.

    1.  Scroll down to the Job parameters section.

    2.  Set the **Run as** field to pa\_admin, pa\_data\_collector or admin roles.

    3.  Verify that the time zone in the **Run As tz** field is appropriate for your organization.

        This timezone is used for the following:

        -   Database queries created for this job
        -   Indicator conditions such as \[\[Created\]\[on\]\[Today\]\]
    4.  Enable the scheduled run of the job by selecting the **Active** checkbox.

4.  Click **Update**.


**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](../application-content-packs/pa-content-pack-essential-safe.md)

