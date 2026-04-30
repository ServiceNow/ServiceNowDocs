---
title: Update the data stored in denormalized tables
description: You can change the number of weeks' worth of data stored in denormalized tables.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring denormalized tables in Field Service Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Update the data stored in denormalized tables

You can change the number of weeks' worth of data stored in denormalized tables.

## Before you begin

Role required: admin

## About this task

**Warning:** You must be a system administrator and a professional developer to complete this procedure.

You can have a maximum total of 20 weeks' worth of data stored in denormalized tables, that includes the current week. For example, you can change the number of weeks from the default to 4 weeks in the past, and 10 weeks in the future, which would total 15 weeks worth of data stored in denormalized tables.

By default, the number of past weeks worth of data stored in denormalized tables is two weeks. By default, the number of future weeks worth of data stored in denormalized tables is 8 weeks.

If you customize and add data to Field Service Management from an external source, or enable or disable Workforce Optimization then you must follow the steps below.

## Procedure

1.  Navigate to **All**, type `sys_properties.list`, and press Enter.

2.  Search for and select the denormalized table system property \(sn\_fsm.wm\_weekly\_resource\_span\).

3.  Set the value to **false**, and select **Update**.

4.  Choose from the following options:

    -   Search for and select sn\_fsm.wm\_weekly\_resource\_span.number\_of\_ weeks\_in\_past – to change the number of weeks worth of data stored in the past.
    -   Search for and select sn\_fsm.wm\_weekly\_resource\_span.number\_of\_weeks\_in future – to change the number of weeks worth of data stored in the future.
    -   Add an external data source.
    -   Enable or disable Workforce Optimization.
5.  Update the value from the default to the new number if you are changing a property value, and select **Update**.

6.  Use the background script to truncate the weekly resource span table.

7.  Search for and select the denormalized table system property \(sn\_fsm.wm\_weekly\_resource\_span\).

8.  Set the value to **true**, and select **Update**.


