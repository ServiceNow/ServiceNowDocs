---
title: Viewing table rules
description: View a summary and execution history of the data management rules that have been created on a table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer]
---

# Viewing table rules

View a summary and execution history of the data management rules that have been created on a table.

## Key benefits

-   View the current number of active and inactive data management rules on the table.
-   Track the backlog of records that meet the requirements of a data management rule but haven't been processed yet.
-   View rule execution history for the last seven days.
-   View a detailed list of the table's data management rules. Select a rule to view a detailed summary.

![A summary of the data management rules on the current table.](../image/dmc-table-rules.png "Viewing data management rules on a table")

## Required ServiceNow AI Platform roles

The admin role is required to view the Data Management Console.

## Accessing table rules in the Data Management Console

Access rules for a specific table in the Data Management Console by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; **Tables**, selecting the table, and then selecting the **Rule details** sub-tab.

## Rules

View a list of the data management rules on the current table.

-   Determine whether a rule is active or inactive by checking the **Status** column.
-   View the types of rules that are configured by checking the **Type** column.
-   Monitor the number of records that meet the conditions for a rule but haven't been processed yet by checking the **Records in backlog** column. Data in this column is refreshed once daily.
-   View a summary of records in the backlog and rule execution history by selecting a rule in the list.

## Total rules

View the total number of data management rules created on the current table, including the number of active and inactive rules. Manage the growth of data in the current table by creating data management rules or adjusting current rule conditions.

-   Create a table cleaner rule to delete older or unwanted records by selecting **New cleanup rule**. See [Create a table cleanup rule](../task/activate-table-cleanup.md).
-   Create an archive rule to move data that's no longer needed every day to an archive table by selecting **New archive rule**. See [Create an archive rule](../../database-rotation/task/t_CreateAnArchiveRule.md#).

## Records in backlog

Track the count of records in the current table that meet the requirements of a data management rule but haven't been processed yet.

-   Track the progress of different types of data management rules over time.
-   Monitor data management rule efficiency and consider adjusting the conditions based on the trend in the backlog record count.
-   Check for bottlenecks that indicate a large number of records in the backlog waiting to be processed.
-   Look for spikes in the backlog across different types of data management rules. Consider scheduling rules at different times to avoid an influx of backlog records.

## Rules executed in the last 7 days

View a list of recent rule activities on the current table. Filter the list by rule type and view the number of affected records for each executed rule.

