---
title: Activate Data Collection for ITOM
description: Activate the Data Collection Pack for ITOM after you enable and configure it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection Content Pack for ITOM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Activate Data Collection for ITOM

Activate the Data Collection Pack for ITOM after you enable and configure it.

## Before you begin

Monthly Data collection within Performance/Performance Analytics runs on a schedule.

**Important:** To get data collection up and running, perform the monthly setup only once.

Role required: admin, pa\_admin, or pa\_data\_collector

## Procedure

1.  Navigate to **Performance/PlatformAnalytics** &gt; **Data Collector** &gt; **Jobs**, and then open **Impact VM – ITOM - Monthly Data Collection**.

2.  Select **Active**, and then update the record.

    **Important:** For monthly job execution, you should not make changes to the Day \(of the month\) and the Time \(of the day\) of the job. Time of the day is determined based on the system time zone. You should keep the default schedule as it works best with the current frequencies of the indicators.

3.  To do a trial run of the monthly data collection, select **Execute Now**.

4.  Navigate to **Performance/Platform Analytics** &gt; **Dashboard**, and then open **Impact VM – ITOM**.

    There are two tabs: Monthly – ITOM and Quarterly – ITOM.

5.  To validate the scores on the dashboard, compare them with the numbers you get from applying the same filters conditions on the fact table.

6.  To run historical jobs, do the following:

    1.  Navigate to **Performance/Platform Analytics** &gt; **Data Collector** &gt; **&gt;Jobs**, and then open **Impact VM – ITOM – Historical Data Collection**.

        **Important:** Do NOT select Active as Historical Data collection within Performance/Platform Analytics runs on an on-demand basis.

        For historical job execution, adjust the Relative start months according to the available data.

        -   If you do not have a full version of Performance/Platform Analytics, historical data won’t be captured beyond 180 days from the job execution date.
        -   If you have the full version of Performance/Platform Analytics, you can change the Relative start date to a longer timeframe than 6 months. For example, you could change Relative start from 6 months ago to 12 months ago.
    2.  Select **Execute Now** to run the historical data collection job.

    3.  Navigate to **Performance/Platform Analytics** &gt; **Dashboard**, and then open **Impact VM – ITOM**.

        There are two tabs: Monthly - ITOM and Quarterly - ITOM. To validate historical data for any specific indicator, select the widget on the dashboard.


