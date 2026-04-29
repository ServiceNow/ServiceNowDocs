---
title: Data Management overview
description: View a summary of your data usage and manage the growth of data on your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data Management overview

View a summary of your data usage and manage the growth of data on your instance.

## Key benefits

-   View a summary of primary storage used on your instance and monitor data usage over time.
-   Determine which tables are consuming the most amount of storage on your instance.
-   Manage the growth of data on your instance directly from the Data Management Console.

![Overview in the Data Management Console.](../image/dmc-overview.png "Overview of data management on your instance")

## Required ServiceNow AI Platform roles

The admin role is required to view the Data Management Console.

## Accessing overview information in the Data Management Console

Access overview information on the **Overview** tab in the Data Management Console by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**.

## Primary storage used

View a summary of primary storage used on your instance. Note that efforts to reduce the amount of primary storage used on your instance might not be reflected until the system completes synchronization.

-   View the total amount of primary storage used on your instance.
-   Track storage usage on your instance over time by viewing the percentage increase or decrease since a specific date.

## Data usage trend

Monitor the top ten tables consuming the most amount of storage on your instance over time.

-   Determine if usage has increased or decreased over time in a weekly or monthly view.
-   Compare the total amount of primary storage used on your instance to the total amount of storage used by the largest tables on your instance.
-   Compare usage between the top ten largest tables on your instance over time.

## Top tables to review

To effectively manage the growth of data on your instance, review the tables that are currently growing the most in size and monitor the size of the largest tables on your instance.

In addition, you can gain a more comprehensive understanding of a table's impact on your instance's overall storage usage by monitoring the size of its associated records.

-   A table that contributes to the size of an associated table is considered a driver table.
-   Associated tables store attachments, audit records, and journal entries that are generated when records are created in the driver table.

Review the top tables on your instance in terms of growth and table size, and then combine that information with the associated record size to determine where to focus your data management efforts first.

-   **Tables over 10 GB with the most growth**

    View the tables that are currently growing the most in size. Only tables larger than 10 GB appear in the list.

    -   View the size of tables with the most growth by checking the Table size \(GB\) column.
    -   Monitor the size of records from associated tables by checking the Associated record size \(GB\) column. To reduce the size of associated records, consider creating archive or cleanup rules in the driver table that's contributing to the growth of the associated tables.
    -   View the tables with the most growth over the last 30 days by checking the Growth \(30 days\) column. For tables that are growing at a faster rate than expected, consider creating a new cleanup rule or a new archive rule.
    -   View a table-level summary of data usage by selecting a table in the list.
-   **Largest tables**

    View a list of the largest tables on your instance.

    -   View the largest tables on your instance by checking the Table size \(GB\) column.
    -   Monitor the size of records from associated tables by checking the Associated record size \(GB\) column. To reduce the size of associated records, consider creating archive or cleanup rules in the driver table that's contributing to the growth of the associated tables.
    -   View a table-level summary of data usage by selecting a table in the list.

After reviewing the top tables, start managing the growth of data on your instance.

-   Manage the growth of audit records from the audit management console by selecting **Manage audit config**.
-   Delete older or unwanted records by selecting **New cleanup rule**. See [Create a table cleanup rule in Core UI](../task/activate-table-cleanup.md).
-   Move data that's no longer needed to an archive table by selecting **New archive rule**. See [Create an archive rule in Core UI](../../database-rotation/task/t_CreateAnArchiveRule.md#).

