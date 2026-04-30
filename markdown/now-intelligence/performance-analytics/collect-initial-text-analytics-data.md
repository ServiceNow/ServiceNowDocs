---
title: Collect initial text analytics data
description: When you configure text analytics for an indicator source, no data is available until a relevant data collector job is run. If you have newly created a text analytics configuration, run a special collection job. If you have added indicators to an existing text analytics configuration, run a historical data collection job to collect only text analytics.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Collect initial text analytics data

When you configure text analytics for an indicator source, no data is available until a relevant data collector job is run. If you have newly created a text analytics configuration, run a special collection job. If you have added indicators to an existing text analytics configuration, run a historical data collection job to collect only text analytics.

## Before you begin

Role required: pa\_power\_user or admin

## Procedure

-   On the **Setup Fields** form, if the button is available next to **Save**, **Update**, and **Delete**, click **Run historic collection**.

    This button launches a single-use historical job that collects only text indexes. It is available only when you create a text analytics configuration.

    This job collects data for a period equal to the shortest period for which there is data for any of the indicators in the analysis. For example, if you are running text analysis on five indicators and you have one year of data for four of them but only four months of data for the fifth indicator, four months of text analytics are collected for all five indicators.

-   If you have added an indicator to an existing text analytics configuration, configure and run a historical data collection job.

    1.  Navigate to **Data collection** &gt; **Jobs**.

    2.  Create or edit a historical data collection job as described in [Create or schedule a data collection job](t_CreatASchedDataCollJob.md), with the following characteristics:

        -   Set the **Collect** job parameter to **Text indexes only**.
        -   Set the **Run** job parameter to **On demand**.
        -   Set **Relative start**, **Relative start interval**, **Relative end**, and **Relative end interval** values that are appropriate for the indicators for which you are performing text analytics.
        -   Ensure that the indicators for which you are performing text analytics match the indicators for the collection job.
    3.  Execute the job.


## What to do next

Now that text analytics are configured and initial data is collected, you can create text analysis widgets for the selected indicators. Consider setting text analytics stop words first. Both these stop words and the Zing stop words can apply.

