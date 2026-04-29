---
title: Viewing all tables
description: View a list of all tables on your instance and the number of active data management rules configured on each table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Viewing all tables

View a list of all tables on your instance and the number of active data management rules configured on each table.

## Key benefits

-   View tables on your instance in terms of size by checking the **Table size \(GB\)** column.
-   Determine which tables have grown the most in size over the last thirty days by checking the **Growth \(30 days\)** column.
-   Determine how many archive, cleanup, and one-time delete rules are active for each table by checking the **Active rules** column.

By default, the list of tables is filtered to show tables over 100 MB in size.

![Tables view in the Data Management Console.](../image/dmc-tables.png "Viewing tables in the Data Management Console")

## Required ServiceNow AI Platform roles

The admin role is required to view the Data Management Console.

## Accessing the Tables view in the Data Management Console

Access table information in the Data Management Console in one of the following ways: You can also access the **Tables** tab by selecting View additional tables on the Overview tab.

-   Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console** and select the **Tables** tab.
-   Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console**. On the **Overview** tab, select **View additional tables**.

## Use cases

-   Monitor data usage for physical tables, including the Task \[task\] table.
-   Monitor data usage for logical tables, including the Incident \[incident\], Problem \[problem\], and Change Request \[change\_request\] tables.
-   Access data usage and rule details by selecting a table in the list. See [Viewing data usage by table](data-management-table-data.md).

