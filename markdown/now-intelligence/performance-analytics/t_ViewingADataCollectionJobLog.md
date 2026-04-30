---
title: View the data collection job logs
description: Job logs display information about the data collection jobs that have run for Performance Analytics. You can view job logs, create events, and view and edit the event registry. The list view displays all log entries, unless filtered.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data collection process and logging, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# View the data collection job logs

Job logs display information about the data collection jobs that have run for Performance Analytics. You can view job logs, create events, and view and edit the event registry. The list view displays all log entries, unless filtered.

## Before you begin

Role required: pa\_data\_collector or admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Job Logs**.

    The log provides the following information for all occurrences.

    |Field|Description|
    |-----|-----------|
    |Created|Date and time the data collection job started.|
    |State|One of the following values: **Collecting**, **Collected**, or **Collected with errors**.|
    |Name|Name of the job.|
    |Completed|Date and time the data collection job ended.|
    |Inserts|The number of new records that have been inserted.|
    |Updates|The number of existing records that have been updated.|
    |Warnings|The number of warnings that occurred during the data collection process.|
    |Errors|The number of errors that occurred during the data collection process.|
    |Run time|Duration of the job.|

2.  Click **Created** to view the details of a specific job.

    Additional information on the job settings and sequence steps is displayed. If notifications are enabled, you can send emails about the data collection results to users.


## What to do next

Click on a job in the list to see a detailed log of the job. For information about the contents of individual job logs, see [Log details for classic data collector](../reference/original-data-collection-process.md) .

**Note:** If the logs return the following error, `java.lang.IllegalStateException: Sparse storage format has one field, sys_id`, see [KB0550063](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0550063).

**Parent Topic:**[Data collection process and logging](../concept/data-collection-process-logging.md)

**Related topics**  


[View a data collection job event](t_ViewingADataCollectionJobEvent.md)

