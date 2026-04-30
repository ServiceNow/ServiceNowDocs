---
title: Schedule an assessment
description: After you have evaluated your questionnaires using on-demand assessments, edit your categories and metrics as needed, reset your metric type record, and select the users who are qualified to evaluate the assessable records.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scheduled assessments, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Schedule an assessment

After you have evaluated your questionnaires using on-demand assessments, edit your categories and metrics as needed, reset your metric type record, and select the users who are qualified to evaluate the assessable records.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Open the metric type you created for the [on-demand assessment](t_OnDemandAssessment.md) and set the **Schedule type** to **Scheduled**.

2.  Make sure the categories and metrics you created for the on-demand assessment are correct.

3.  Create [category users](../reference/r_CategoryUsersAndStakeholders.md) who have special knowledge of your categories.

4.  Create [stakeholders](../reference/r_CategoryUsersAndStakeholders.md) by associating category users to specific assessable records.

5.  [Set a schedule](t_SetAssesstGenerationSchedule.md) for automatic assessment generation or [generate the assessment manually](t_GenAVendorTypeAssmtManually.md).

    **Note:** This procedure must be done by a system administrator.

6.  Configure [email notifications](../reference/r_AssessmentNotifications.md) to remind users of their assigned assessments and to report to managers when an employee misses an assessment deadline.

7.  Analyze the assessment ratings in an assessment scorecard or decision matrix.


**Parent Topic:**[Scheduled assessments](../concept/c_ScheduledAssessments.md)

**Related topics**  


[Assessments](../reference/r_Assessments.md)

