---
title: Cleaning collected Performance Analytics data
description: Performance Analytics scores and snapshots may grow over time and should be routinely cleaned to ensure optimal performance and accurate data.Modify the scheduled job to configure when Performance Analytics scores and snapshots are cleaned. The scheduled cleanup job should not run while a data collection job is running.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Cleaning collected Performance Analytics data

Performance Analytics scores and snapshots may grow over time and should be routinely cleaned to ensure optimal performance and accurate data.

Performance Analytics uses a scheduled job to remove old scores and snapshots.

The Clean PA collections scheduled job is active by default and has no impact on performance. By default, the job runs daily so it only has to delete a small amount of data.

**Note:** The dictionary attributes nibble\_size and nibble\_sleep affect the behavior of the collection cleaner job if the attributes are defined for one of the Score \(pa\_scores, pa\_scores\_l1, pa\_scores\_l2\) tables or the Snapshot \(pa\_snapshots\) table. For more information, see Altering tables and fields using dictionary attributes.

**Related topics**  


[bundle-platadm.c_DictionaryAttributes]

[KB0720725: Clearing Performance Analytics Score data](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0720725)

## Modify the Clean PA collections job

Modify the scheduled job to configure when Performance Analytics scores and snapshots are cleaned. The scheduled cleanup job should not run while a data collection job is running.

### Before you begin

Role required: pa\_admin or admin

### About this task

By default, the Clean PA collections job runs at 05:00 which is appropriate when using the default data collection jobs. If you create additional data collection jobs, you may need to change the start time of the Clean PA collections job.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Automation** &gt; **Schedules**.

2.  Select the **Clean PA collections** job.

3.  Make any necessary changes.

    For example, change the **Run time** field value to change when the job runs.

4.  Click **Update**.


**Related topics**  


[bundle-platadm.c_ScheduledJobs]

[KB0721309: Configuring the Performance Analytics Table Cleaner](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0721309)

