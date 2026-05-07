---
title: Schedule metadata collector runs
description: Schedule a metadata collector to run automatically at a specified frequency.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Running metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Schedule metadata collector runs

Schedule a metadata collector to run automatically at a specified frequency.

## Before you begin

Role required: connection\_admin

## About this task

Configure collection schedules to maintain up-to-date catalog metadata without manual intervention. Scheduled runs execute automatically and refresh data assets with current information from source systems. Schedule frequency should balance freshness requirements against system load and source system availability.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub icon in the left sidebar.

3.  Select **Connectors**.

4.  Select **Metadata collector**.

5.  Select the metadata collector you want to schedule to run automatically.

6.  In the **Runtime schedule** section, set the fields.

    |Field|Description|
    |-----|-----------|
    |Frequency|How often the collector runs, such as daily or weekly.|
    |Time|Time of day to run the collector, in 24-hour format.|
    |Repeat on|Days of the week on which the collector runs. Applies only when Frequency is set to Weekly.|

    **Note:** Schedule collections during low-usage periods to minimize impact on source systems.

7.  Select **Save**.![](../image/dc-mcollector-schedule.png)


**Parent Topic:**[Running metadata collectors](../concept/run-metadata-collectors-dc.md)

