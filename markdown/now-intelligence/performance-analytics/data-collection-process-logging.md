---
title: Data collection process and logging
description: Performance Analytics data collection jobs collect indicator scores. To debug data collection, it is helpful to understand the data collection process and how it is reflected in the job logs.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data collection process and logging

Performance Analytics data collection jobs collect indicator scores. To debug data collection, it is helpful to understand the data collection process and how it is reflected in the job logs.

As an administrator, sometimes you have to debug a data collection job. Each job generates a log, but to understand the entries in this log, you must know which step in the data collection process produced the entries. Performance Analytics provides three levels of log:

-   Job events, which show which jobs have been executed.
-   Job logs, which provide an overview of each executed job.
-   Job log details, which describe what happened in each step of an executed job.

The Admin Console also provides daily, weekly, and monthly overviews of data collection jobs.

-   **[Optimizing data collection](optimized-data-collection.md)**  
The optimized Performance Analytics data collector reduces the time, memory, and CPU usage for processing large data sets.
-   **[View a data collection job event](../task/t_ViewingADataCollectionJobEvent.md)**  
Job events show which jobs have been executed for Performance Analytics and which actions have been triggered in your ServiceNow instance, such as notifications or business rules.
-   **[View the data collection job logs](../task/t_ViewingADataCollectionJobLog.md)**  
Job logs display information about the data collection jobs that have run for Performance Analytics. You can view job logs, create events, and view and edit the event registry. The list view displays all log entries, unless filtered.
-   **[Log details for optimized data collector](../reference/log-details-optimized-dc.md)**  
Starting with the Tokyo release, a new, optimized data collector is available. The log details for this data collector differ from the log details of the classic data collector.
-   **[Log details for classic data collector](../reference/original-data-collection-process.md)**  
Performance Analytics score collection follows the process described here. To aid troubleshooting, a mapping between job steps and log entries is provided.
-   **[View data collection usage](../task/view-data-collection-usage-statistics.md)**  
To view statistics about data collection jobs, click **Data Collection Overview** in the Usage tile on the Performance Analytics Admin Console.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

