---
title: Data archiving
description: Migrate data that's no longer needed every day from a primary table to an archive table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data archiving

Migrate data that's no longer needed every day from a primary table to an archive table.

## Key benefits

-   Free up system resources and avoid performance issues in queries and reports by migrating older records into an archive table.
-   Preserve data for auditing or historical purposes.
-   Delete archived data after a specified period using a destroy rule.

![Sample Benefits of Archiving Data](../image/SampleBenefitsOfArchivingData.png "Sample Benefits of Archiving Data")

## Accessing archive rules

You can define and access the archive rules for a table by navigating to **All** &gt; **System Data Management** &gt; **Data Management Policies** and selecting the data management policy for the table.

## Use cases

-   The longer an instance runs, the more likely it is to accumulate data that is no longer relevant. For example, task records from two years ago are typically less relevant than currently active tasks. Old data may eventually cause performance issues by consuming system resources and slowing down queries and reports. You can archive records in core tables such as the Task \[task\] table and records in custom tables that you create on the ServiceNow AI Platform.
-   Archive records when table queries are slow. For example, assume the Incident \[incident\] table on your instance has grown and users are reporting that queries against the table are slow. You can create an archive rule with conditions like **\[Closed\] \[relative\] \[on or before\] \[150\] \[Days\] \[ago\]** and **\[Active\] \[is\] \[false\]** to move records to the Archived Incidents \[ar\_incident\] table when they're closed for more than 150 days.
-   Archive records in a primary table, including any records in other tables that reference those records. For example, you can archive records in the Problem \[problem\] table, and include any incidents that reference a problem record in the Problem in Incident field.

For information about using the data archive feature, see [Archiving records in Core UI](../../managing-data/concept/archiving-older-records.md).

## Archiving data in object storage with RaptorDB Professional V2

When you upgrade to RaptorDB Professional V2 and activate the Data Archiving \(com.glide.db.columnar.archive\) plugin, the archiving process transitions to a modern, columnar storage model. Archived records and attachments are migrated from the primary instance to a dedicated secondary object storage, but remain accessible in the same way as regular tables.

Object storage doesn't require additional configuration beyond plugin activation, and is exclusive to RaptorDB Professional V2. For more information about upgrading to RaptorDB Professional, contact your account representative.

Object storage benefits:

-   **Columnar and off-instance storage**

    Archived data is stored in a columnar format outside the primary instance, freeing up primary storage and improving query performance for active data.

-   **Continued accessibility**

    Archived records remain accessible to users on the ServiceNow AI Platform, ensuring that historical data can be queried and reported on as needed.

-   **Scalable storage capacity**

    The object storage archive provides greater storage capacity, allowing you to maintain larger archives without impacting primary database performance.

-   **Separation of archive and active data**

    By migrating archive records off-instance, the solution reduces primary storage consumption and supports long-term data retention strategies.


During the migration to object storage, data management processes that interact with archive tables, like data archiving and table cleaner, are temporarily paused. However, no downtime is required for the upgrade itself. For information about activating the Data Archiving \(com.glide.db.columnar.archive\) plugin after upgrading to RaptorDB Professional V2, see: [Activate data archiving to object storage](../../managing-data/task/activate-columnar-storage.md).

