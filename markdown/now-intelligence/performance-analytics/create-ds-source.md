---
title: Create a Data snapshots source
description: To provide a filtered dataset of records that you can evaluate with one or more indicators, create an indicator source. Data snapshots indicators require different sources than do classic indicators. Data snapshots logs are accessible on the source records.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Data snapshots logs, logs]
breadcrumb: [Data snapshots sources and collection, Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a Data snapshots source

To provide a filtered dataset of records that you can evaluate with one or more indicators, create an indicator source. Data snapshots indicators require different sources than do classic indicators. Data snapshots logs are accessible on the source records.

## Before you begin

Role required: pa\_data\_collector or higher

## Procedure

1.  Select the application scope.

    The Data snapshots source inherits your application scope. With this Data snapshots source, you can only create indicators in that application scope. You can only create one Data snapshots source for a fact table, so the choice of application scope is important. For more information, see Application scope.

2.  Navigate to **All** &gt; **Data Snapshots** &gt; **Sources**.

3.  Select **New**.

4.  Select a fact table from the list.

    You can select only from tables that support the change data capture \(CDC\) process.

5.  Select either a Daily data frequency or All Activity.

    The Daily frequency supports only the standard calendar and the Daily indicator frequency. All Activity includes the standard calendar and all business calendars for which a Business Calendar Group is defined. It supports all indicator frequencies defined in those business calendars including intraday frequencies such as Work Shift. All Activity also supports showing data from incomplete periods in data visualizations and KPI Details. For more information, see Creating business calendars.

6.  Select which **Fields** of the fact table to include in the Data snapshots source.

    Only the fields you specify in the Data snapshots source are tracked historically, or can be used to filter the resulting indicators. You can add more fields after creating the Data snapshots source. However, you won't have data about fields from before you added them. Nor can you remove fields.

    **Note:** If you add a field that references a table with a record hierarchy, you can roll up the scores for that hierarchy through a [hierarchical dashboard filter](../../par-for-workspace/concept/create-hierarchical-filter.md) or in [KPI Details](../../par-for-workspace/task/filter-data-snapshots-indicator-scores.md).

7.  To activate data mining for the Data snapshots source, turn on **Data collection enabled**.

    You can turn data collection off and on after creating the Data snapshots source. However, doing so might create data gaps and inconsistencies in your indicator scores.


## What to do next

After you create the Data snapshots source, only **Data collection enabled**, **Fields**, and **Data retention period** are editable.

Track the data collection activity in the log entries on this record.

**Parent Topic:**[Data snapshots sources and collection](../reference/tables-unlimited-breakdowns.md)

