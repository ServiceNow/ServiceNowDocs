---
title: Generate an on-demand assessment for multiple assessable records
description: When you generate an on-demand assessment from the Assessment Metric Type form, the resulting assessment contains questions from all categories associated to any assessable records for the metric type.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [On-demand assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate an on-demand assessment for multiple assessable records

When you generate an on-demand assessment from the Assessment Metric Type form, the resulting assessment contains questions from all categories associated to any assessable records for the metric type.

## Before you begin

Role required: assessment\_admin or admin

Publish the assessment.

## About this task

For example, if there are 15 assessable records associated to at least one category with assessment metrics, the assessment contains questions for all 15 assessable records.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Open a metric type that has the **On demand** schedule type.

3.  To assign the assessment to users configured in the **Assessors** tab of the assessment, and other specified users, perform these steps.

    1.  On the Assessment Metric Type form, click **Assign Assessment**.

    2.  Select a user from the Recent Assessors list or select a different user.

    3.  Click **OK**.

4.  To assign the assessment to users configured in the **Assessors** tab of the assessment, click **Assign to Assessors**.


## Result

The system generates an assessment instance assigned to the selected users.

**Parent Topic:**[On-demand assessments](../concept/c_OnDemandAssessments.md)

**Related topics**  


[Assessment generation](../concept/c_AssessmentGeneration.md)

[Generate a scheduled assessment manually](t_GenSchedAssessmentManually.md)

[Assessment groups](../concept/c_AssessmentGroups.md)

[Clean up assessment data](t_CleanUpAssessmentData.md)

