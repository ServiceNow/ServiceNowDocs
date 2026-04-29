---
title: Viewing data usage by table
description: View a summary of data usage for an individual table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analyze data usage, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Viewing data usage by table

View a summary of data usage for an individual table.

## Key benefits

-   Analyze data usage at the table-level.
-   Monitor data usage for a specific table over time.
-   Access a comprehensive view of a table's impact on storage usage by checking the size and record count of driver tables and associated tables.

Details on this page are refreshed once daily.

![Data usage by table.](../image/dmc-data-usage.png "View data usage by table in the Data Management Console")

## Required ServiceNow AI Platform roles

The admin role is required to view the Data Management console.

## Accessing data usage by table in the Data Management Console

Access data usage for a specific table in the Data Management Console by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console** &gt; **Tables** and selecting the table.

## Table size \(GB\)

View the total amount of storage used by the current table. If you've made significant changes to your data recently, it might take up to 24 hours for changes to appear.

Track storage usage over time by viewing the percentage increase or decrease since a specific date.

## Associated table size \(GB\)

Associated tables contain records that don't have a lifespan of their own. Examples include attachments, audits, and journals.

-   View the total amount of storage used by associated tables.
-   Track the rate of storage usage by viewing the percentage change since a specific date.
-   Address growth in associated tables by creating data management rules on the current table.

## Data usage trend

Monitor data usage for the current table over time.

-   Track the size of the current table over weeks or months.
-   Compare data usage between the current table and associated tables over time.

## Driver tables

Driver tables are those that contribute to the size of another table. For example, the Incident \[incident\], Problem \[problem\], and Change Request \[change\_request\] tables contribute to the growth of the Task \[task\] table, which makes them driver tables.

-   Determine which tables are driving volume to the current table.
-   View the size of each driver table and the total record count in each driver table.
-   Address growth in the current table by creating data management rules in the driver tables.

## Associated tables

Associated tables store records like attachments, audit records, and journal entries that don't have a lifespan of their own. For example, the Sys Audit \[sys\_audit\], Attachment \[sys\_attachment\], and Journal Entry \[sys\_journal\_field\] are tables associated with the Incidents table, which contributes volume to these tables.

-   Determine how much volume the current table is contributing to associated tables.
-   View the size of associated records and the total record count in each associated table.
-   Address growth in associated tables by creating data management rules on the current table.

