---
title: Process Mining data cleanup
description: The Process Mining properties page provides configuration options for Process Mining.Set properties that determine how long Performance Analytics projects are maintained before being deleted by the scheduled cleanup job.Schedule a job to delete older backup versions and clean up cluster analysis records by executing the scheduled script ProminVersionCleanup.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Process Mining, Process Mining, Platform Analytics]
---

# Process Mining data cleanup

The Process Mining properties page provides configuration options for Process Mining.

**Parent Topic:**[Configuring Process Mining](setting-up-process-mining.md)

## Data cleanup properties

Set properties that determine how long Performance Analytics projects are maintained before being deleted by the scheduled cleanup job.

These properties are available for Process Mining.

<table id="table_u43_ldx_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define the number of days to persist PA Projects \(Project Definition\) from the last updated date **promin.persist.pa\_model**

</td><td>

Set the number of days that Performance Analytics \(PA\) Projects will be kept after the last date it was updated.-   Type: integer
-   Default value: 30 \(days\)
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Define the number of days to retire projects due to inactivity **promin.auto\_retire\_days**

</td><td>

Set the number of days of inactivity after which the projects will be retired.-   Type: integer
-   Default value: 90 \(days\)
-   Location: Process Mining &gt; **System** &gt; **Properties**

</td></tr><tr><td>

Define the number of days to clean up retired projects **promin.auto\_clean\_days**

</td><td>

Set the number of days post retirement after which the projects will be cleaned up. However, the project configuration will be retained.-   Type: integer
-   Default value: 90 \(days\)
-   Location: Process Mining **System** **Properties**

</td></tr></tbody>
</table>**Related topics**  


[Example of an indicator using Process Mining](performance-analytics-using-process-mining.md)

## Schedule job for version cleanup

Schedule a job to delete older backup versions and clean up cluster analysis records by executing the scheduled script **ProminVersionCleanup**.

### Before you begin

Role required: administrator

### About this task

When regenerating projects, the **ProminVersionCleanup** job deletes obsolete, cached statistics. The older statistics move into a previous version, while the new version is created for the updated project.

When regenerating or deleting projects, this job cleans records created during cluster analyses.

### Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Background Jobs**.

2.  Select the scheduled job **ProminVersionCleanup**.

3.  Check or set the following.

4.  1.  Enable the **Active** check box.
2.  Check if the Run field is **Daily**.
3.  Set the Time in hours.
5.  Select **Execute Now**.


### Result

Backup version and cluster record cleanup execute daily.

