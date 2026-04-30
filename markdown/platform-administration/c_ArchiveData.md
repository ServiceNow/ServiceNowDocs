---
title: Data archiving
description: Move data that's no longer needed every day from a primary table to an archive table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Explore, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data archiving

Move data that's no longer needed every day from a primary table to an archive table.

## Key benefits

-   Free up system resources and avoid performance issues in queries and reports by moving older records into an archive table.
-   Preserve data for auditing or historical purposes.
-   Delete archived data after a specified period using a destroy rule.

![Sample Benefits of Archiving Data](../image/SampleBenefitsOfArchivingData.png "Sample Benefits of Archiving Data")

## Accessing archive rules

You can define and access archive rules for a table by navigating to **All** &gt; **System Data Management** &gt; **Data Management Policies** and selecting the data management policy for the table.

## Use cases

-   The longer an instance runs, the more likely it is to accumulate data that is no longer relevant. For example, task records from two years ago are typically less relevant than currently active tasks. Old data may eventually cause performance issues by consuming system resources and slowing down queries and reports. You can archive records in core tables such as the Task \[task\] table and records in custom tables that you create on the ServiceNow AI Platform.
-   Archive records when table queries are slow. For example, assume the Incident \[incident\] table on your instance has grown and users are reporting that queries against the table are slow. You can create an archive rule with conditions like **\[Closed\] \[relative\] \[on or before\] \[150\] \[Days\] \[ago\]** and **\[Active\] \[is\] \[false\]** to move records to the Archived Incidents \[ar\_incident\] table when they're closed for more than 150 days.
-   Archive records in a primary table, including any records in other tables that reference those records. For example, you can archive records in the Problem \[problem\] table, and include any incidents that reference a problem record in the Problem in Incident field.

For information on using the data archive feature, see [Archiving records](../../managing-data/concept/archiving-older-records.md).

