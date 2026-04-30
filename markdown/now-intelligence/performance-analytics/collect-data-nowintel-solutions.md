---
title: Collect data for Platform Analytics Solutions
description: After you install an Platform Analytics Solution and ensure that it points at the correct data structures in your instance, collect the data for the indicators and breakdowns.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Analytics solutions, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Collect data for Platform Analytics Solutions

After you install an Platform Analytics Solution and ensure that it points at the correct data structures in your instance, collect the data for the indicators and breakdowns.

Whenever you activate an Platform Analytics Solution, you automatically install Data Collector jobs for that Solution. These Data Collector jobs collect analytics information for the indicators and breakdowns in the Solution. After the jobs run, you can see the data in the widgets and dashboards for the Solution. Technically, the Data Collector jobs do the following actions:

-   Run periodically, usually daily
-   Read your operational tables
-   Measure the data for the period \(usually a day\) against the definitions that the indicators and breakdowns specify
-   Store the resulting measurement scores and \(optionally\) raw data in Performance Analytics tables.

The plugin or ServiceNow Store application for an Platform Analytics Solution usually installs the following two jobs:

-   **Historic Data Collection**

    Run the historic Data Collector job when you first install an Platform Analytics Solution. By default, the historic Data Collector job collects the last 60 days of data for the indicators specified in the job. If you want to go back further in time, you can configure the job to collect more historic data. A historic Data Collector job overwrites all data for the period of collection. Therefore, run it only once, when you first install the Platform Analytics Solution. Run a periodic Data Collector job for all subsequent data.

-   **Periodic Data Collection \(usually daily\)**

    This job populates the Performance Analytics tables with data going forward. Schedule the periodic data collector to run with the same periodicity as the frequency of the indicators for which it collects data. Most indicators have a Daily frequency, so most Data Collector jobs also run daily. After you schedule the job, verify that it is Active, or it will not run.


1.  [Run historical data collection for a Platform Analytics Solution](../task/historical-data-nowintel-solution.md)  
After you activate an Platform Analytics Solution, run a historical data collection job. This job gives you immediate insight from your existing data.
2.  [Schedule data collection for a Platform Analytics Solution](../task/schedule-job-nowintel-solution.md)  
Enable the periodic data collection job for your Platform Analytics Solution. Check that the time that it runs is correct.

**Parent Topic:**[Platform Analytics solutions](../../dashboards/concept/content-packs-in-form-analytics-published.md)

**Related topics**  


[Collecting indicator scores](c_ClctData.md)

