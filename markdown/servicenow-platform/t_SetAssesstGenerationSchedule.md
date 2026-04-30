---
title: Set an assessment generation schedule
description: You can set assessment generation schedules. You must set a schedule for each metric type individually.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scheduled assessments, Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set an assessment generation schedule

You can set assessment generation schedules. You must set a schedule for each metric type individually.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Open the appropriate metric type record.

3.  Click the reference icon next to the **Scheduled job** field to open the Schedule Item record.

4.  Locate the **Trigger type** field and set a recurring schedule for the scheduled job.

    For example, if you want to generate assessment components each month, select the **Interval** or **Repeat** trigger type and specify a **Repeat** value of 30 days. Alternatively, select **Day in Month** and specify a Run time and Run day of month.

    The optimal frequency of assessment generation is subjective. When you set the schedule, keep in mind the number of records to evaluate, how often your organization requires updated assessment results, the time and effort required of users to complete assessments, and other relevant factors.


**Parent Topic:**[Scheduled assessments](../concept/c_ScheduledAssessments.md)

