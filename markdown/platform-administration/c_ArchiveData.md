---
title: System Archive
description: System Archive enables you to manage table growth by moving inactive records out of primary tables into dedicated archive tables within the same instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# System Archive

System Archive enables you to manage table growth by moving inactive records out of primary tables into dedicated archive tables within the same instance.

System Archive is a platform feature that's available on all the ServiceNow instances.

![Difference between System Archive and Live Archive processes](../image/system-archiving-and-live-archive.png)

## Key benefits

-   Releases system resources, which improves query and report performance.
-   Preserves data for auditing or historical purposes.
-   Deletes archived data after a specified period using a destroy rule.

Note that System Archive does not reduce primary storage usage or move data to a separate storage tier. For information about moving records off the primary database to an object storage, see [Live Archive with RaptorDB Professional V2](data-archiving-with-raptordb-professional-v2.md).

![Archiving data within the instance using System Archive](../image/SampleBenefitsOfArchivingData.png)

## Archive rules

During archiving, records that meet the defined archive rules are moved to a corresponding archive table prefixed with `ar_`. For more information, see [Viewing table rules](../../managing-data/concept/data-management-table-rules.md) and [Viewing rule activities](../../managing-data/concept/data-management-rule-activities.md).

## Use cases

-   Instances that have been running for a long time and have accumulated data that is no longer relevant. For example, task records from two years ago are typically less relevant than currently active tasks. This old data can eventually cause performance issues by consuming system resources and slowing down queries and reports. You can archive records in core tables such as the Task \[task\] table and records in custom tables that you create on the ServiceNow AI Platform.
-   The Incident \[incident\] table on your instance has grown and users are reporting that queries against the table are slow. You can create an archive rule with conditions like **\[Closed\] \[relative\] \[on or before\] \[150\] \[Days\] \[ago\]** and **\[Active\] \[is\] \[false\]** to move records to the Archived Incidents \[ar\_incident\] table when they're closed for more than 150 days.
-   Archive related records together to maintain data integrity for compliance and auditing requirements. This approach archives records from a primary table along with any dependent records in other tables that reference them. For example, when archiving records from the Problem \[problem\] table, you can include incidents that reference those problem records in the **Problem in incident** field.

For information about using the System Archive feature, see [Archiving records in Core UI](../../managing-data/concept/archiving-older-records.md).

