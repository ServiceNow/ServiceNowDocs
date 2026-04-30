---
title: Clean up assessment data
description: The assessment process generates a considerable amount of data, some of which is not useful after a short time.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scheduled assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Clean up assessment data

The assessment process generates a considerable amount of data, some of which is not useful after a short time.

## Before you begin

Role required: assessment\_admin or admin

## About this task

The assessment process generates a considerable amount of data, some of which is not useful after a short time. Assessments include a scheduled job called **Remove Old Assessment Data** that is available to administrators only. The scheduled job removes these items if they are more than a year old:

-   Assessment instance questions
-   Assessment instances
-   Metric results

By default, the scheduled job is executed manually. Administrators can configure the scheduled job to run automatically on a recurring schedule.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

2.  Open the **Remove Old Assessment Data** record.

3.  On the Schedule Item form, set the **Trigger type** field to run the scheduled job on a recurring schedule.

    It is recommended to set the scheduled job to run on a weekly or monthly basis.

4.  Click **Execute Now** to run the scheduled job.


**Parent Topic:**[Scheduled assessments](../concept/c_ScheduledAssessments.md)

