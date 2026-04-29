---
title: Configuring Article Optimization jobs
description: Article Optimization jobs are used to define a schedule to run scans along with their conditional settings, if any. Each job will have one or more scans associated with it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Article Optimization jobs

Article Optimization jobs are used to define a schedule to run scans along with their conditional settings, if any. Each job will have one or more scans associated with it.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center** &gt; **Lists** &gt; **Article Optimization** &gt; **Jobs**.

2.  Select **New**.

    1.  If you want to clone and modify an existing job, go to the **sysauto\_kb\_assist\_job** table.

    2.  Open a record and select **Insert and stay** to copy the scan.

    3.  **Rename** the copied scan.

3.  Fill out the record form as follows:

    1.  Set the **Query table** field to **Knowledge** \(or another table used to store knowledge articles\).

    2.  Define the filter criteria for the job in the **Query conditions** field.

4.  Define the schedule of the job in the **Run** field and refine it using the **Time Zone** and the **Time** fields \(to stagger job run times and avoid performance issues\).

5.  **Save** the record.

6.  Add or delete scans on the job from the **Related Article Assist Scans** related list.


## Result

The article optimization job is configured.

