---
title: Set the Schedule optimization logging level
description: Adjust the logging level settings to specify the detail included in the Schedule Optimization logs.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring log levels for detailed optimization analysis, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Set the Schedule optimization logging level

Adjust the logging level settings to specify the detail included in the Schedule Optimization logs.

## Before you begin

Role required: wm\_admin

## About this task

Each logging level option includes the information from the preceding levels. For example, selecting 'Info' will display 'Error' and 'Warning' logs as well, while 'Debug' will include logs from 'Error,' 'Warning,' and 'Info'.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**.

2.  In the **Logging level** field, select the desired logging level.

    |Logging Level|Description|
    |-------------|-----------|
    |**Error**|Critical errors that lead to significant issues, preventing optimization from running successfully.|
    |**Warning**|Warning alerts for failed validations.|
    |**Info**|All general information about the run, including its duration and the total number of tasks and agents involved.|
    |**Debug**|Debug messages provide detailed, technical descriptions at the code level, focusing on the configurations, and database queries involved.|

3.  Select **Save**.


**Parent Topic:**[Configuring log levels for detailed optimization analysis](configuring-log-levels-for-detailed-optimization-analysis.md)

