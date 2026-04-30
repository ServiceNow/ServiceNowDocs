---
title: Enable daily data collection for Agile 2.0 dashboards
description: Enable scheduled data collection to begin collecting scores on new data automatically. Data collection jobs automatically collect scores for automated indicators and breakdowns.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Enable daily data collection for Agile 2.0 dashboards

Enable scheduled data collection to begin collecting scores on new data automatically. Data collection jobs automatically collect scores for automated indicators and breakdowns.

## Before you begin

Role required: pa\_admin or admin

## About this task

**Note:** Historical data collection is not supported for the underlying indicators of the \[Scrum\] Daily Data Collection job.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Find and open the \[Scrum\] Daily Data Collection job.

3.  Start the \[Scrum\] Daily Data Collection job.

    1.  Scroll down to the Job parameters section.

    2.  Set the **Run as** field to a user that has one of the following roles: pa\_admin, pa\_data\_collector, or admin roles.

    3.  Verify that the time zone in the **Run As tz** field is appropriate for your organization.

        This timezone is used for the following:

        -   Database queries created for this job
        -   Indicator conditions such as \[\[Created\]\[on\]\[Today\]\]
    4.  Enable the scheduled run of the job by selecting the **Active** checkbox.

4.  Click **Update**.


**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

