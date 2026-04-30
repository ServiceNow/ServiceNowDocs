---
title: Analyze data usage on your instance
description: Monitor data usage over time and determine which tables are consuming the most amount of storage on your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Analyze data usage on your instance

Monitor data usage over time and determine which tables are consuming the most amount of storage on your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console**.

2.  Determine which tables are consuming the most storage in your instance by checking the **Primary storage used \(GB\)** chart.

    ![A summary a of primary storage used by the top 3 tables on your instance.](../image/primary-storage-used.png "Primary storage used")

    -   View a summary of the total amount of primary storage used on your instance.
    -   Compare usage between the top three tables and all other tables on your instance.
    -   Access details in the Physical Table Stats \[sys\_physical\_table\_stats\] table by selecting a portion of the chart.
3.  Monitor the top three tables consuming the most amount of storage over time by checking the **Primary storage trend \(for last month\)** chart.

    ![A trend chart depicting primary storage used by the top 3 tables over the last month.](../image/primary-storage-trend.png "Primary storage trend")

    -   Determine if usage has increased or decreased over time.
    -   Compare usage between the top three tables and all other tables on your instance over time.
    -   Access details in the Physical Table Stats \[sys\_physical\_table\_stats\] table by selecting a line on the trend chart.
4.  View the top 10 tables that are consuming the most storage on your instance.

    -   Sort the top 10 tables by their size in GB.
    -   Access details in the Physical Table Stats \[sys\_physical\_table\_stats\] table for all tables in your instance by selecting **View all**.
5.  Review your data management policies to determine if table data can be archived or cleaned after a point in time.

    -   Determine if table data should be archived using an archive rule or deleted using a table cleaner rule.
    -   If a table doesn't have a data management policy, create a data management policy by selecting **Create Policy**.
    -   View a list of current data management policies on your instance by selecting **View All Policies**.
    -   View a list of current archive rules on your instance by selecting **View Archive Rules**.

