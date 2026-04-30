---
title: Viewing rule activities
description: View a summary of records in the backlog and the execution history for a specific rule on the table in context.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer]
---

# Viewing rule activities

View a summary of records in the backlog and the execution history for a specific rule on the table in context.

## Key benefits

-   View details for a specific data management rule.
-   Track the backlog of records that meet the rule's conditions but haven't been processed yet.
-   View a detailed summary of the rule's execution history.

![Viewing a table's rule activities.](../image/dmc-rule-activities.png "Viewing rule activities")

## Required ServiceNow AI Platform roles

The admin role is required to view the Data Management Console.

## Accessing rule activities in the Data Management Console

Access recent activity for a specific rule in the Data Management Console by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; **Tables**. Select a table, select the **Rule details** sub-tab, and then select a specific rule.

## Rule details

View basic information about a data management rule including the following details:

-   **Table**

    The table to which the data management rule applies.

-   **Data policy**

    The data policy to which the data management rule belongs.

-   **Application scope**

    The application scope of the table.

-   **Type**

    The type of data management rule, such as archive, cleanup, or one-time delete.

-   **Status**

    The current status of the data management rule.


## Records in backlog

View the total number of records that meet the conditions for the rule but haven't been processed yet. The count is updated once a day.

## Trend of backlog records

Track the backlog of records that meet the conditions for the rule but haven't been processed yet.

-   Track the progress of the rule over time.
-   Monitor data management rule efficiency and consider adjusting the conditions based on the trend in the backlog record count.
-   Check for bottlenecks that indicate a large number of records in the backlog waiting to be processed.

## Execution history

View a detailed summary of the rule's execution history.

-   View the date and time a rule was executed by checking the **Execution time** column.
-   Determine how many records were archived or deleted by checking the **Records impacted** column. Consider adjusting the rule's conditions if the number of records isn't sufficient.
-   Determine how long the rule took to complete by checking the **Duration** column.

