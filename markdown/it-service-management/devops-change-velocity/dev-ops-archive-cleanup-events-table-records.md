---
title: Inbound event table data archiving and cleanup
description: Use table cleaners on the inbound events table to purge event data records beyond a specified period. Configure a retention policy with table rotation on the auto-flush form to manage table size growth and archiving data beyond the specified duration.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Inbound event table data archiving and cleanup

Use table cleaners on the inbound events table to purge event data records beyond a specified period. Configure a retention policy with table rotation on the auto-flush form to manage table size growth and archiving data beyond the specified duration.

## Data management

The data management feature allows you to enable archiving and purging of inbound event data. Database rotation and table cleanup configurations are enabled to ensure that eight weeks of event data is retained. Instance performance is preserved using ServiceNow AI Platform features such as Database rotation, [table rotation](https://www.servicenow.com/docs/access?context=c_TableRotation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US), and [table cleanup](https://www.servicenow.com/docs/access?context=table-cleanup&version=zurich&pubname=zurich-application-development&ft:locale=en-US). A scheduled job is auto-enabled two weeks after you upgrade.

## Table rotation on processed inbound events table

The DevOps processed inbound events \[sn\_devops\_processed\_inbound\_event\_list.do\] table contains copies of event data from the DevOps inbound events \[sn\_devops\_inbound\_list.do\] table, that is in state '**processed**' and '**ignored**'.

The processed inbound events table has the table rotation feature enabled. In all, there are eight preconfigured shards, each containing a week's event data from the DevOps inbound event table. By default, once you have 56 days \(7 days\) \(Duration\) \*8 shards \(Rotations\) of data in the processed inbound table, table rotation is activated. For more information on applying table rotation, see [Apply table rotation](https://www.servicenow.com/docs/access?context=t_ApplyTableRotation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Tip:** To modify table rotation configuration, navigate to **System Definitions** &gt; **Table Rotation** and open the record for DevOps processed inbound events table.

## Scheduled jobs and Table cleaners

**Important:** A scheduled job is auto-enabled two weeks after you upgrade . The scheduled job will run every seven days and is deactivated after the last update.

Scheduled jobs activate tables cleaners on the inbound events if either of the following scenarios are met:

-   A week after you upgrade, and the processed inbound table has records older than seven weeks.
-   Two weeks after you upgrade.

The table cleanup feature for the inbound events table \[sn\_devops\_inbound\_table\] has two cleaners that are part of the base system upgrade.

1.  Table cleaners are activated and run on the inbound events \[sn\_devops\_inbound\_table\_list.do\] for events in the following states.

    -   **Processed**
    -   **Ignored**
    based on the value specified in the **Age in seconds** field against the value in `sys_created_on` field.

2.  Table cleaners are activated and run on the inbound events table \[sn\_devops\_inbound\_table\_list\] for events in the following states.

    -   **New**
    -   **Retry**
    -   **In-progress**
    -   **Deferred**
    based on the value specified in the **Age in seconds** field against the value in `sys_created_on` field.


**Note:** By default, table cleaners are run on the inbound events table for these states from the time the schedules jobs are activated. The default value in the **Age in Seconds** field is 4,838,400 seconds \(56\*24\*60\*60\).

## Auto-updates to table cleaner frequency

Events in states **processed** and **ignored** are backed up and copied to the processed inbound events \[sn\_devops\_processed\_inbound\_event\_list\] table. By default, the process cleaners are auto-updated to an interval of 30 minutes or 1800 seconds, on the inbound events table, if the following conditions are met:

-   Two weeks have passed since the scheduled job is active.
-   The processed inbound event table has event data older than 7 weeks.

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

