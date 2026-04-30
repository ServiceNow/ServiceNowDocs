---
title: Enable manager notifications
description: Users with the assessment\_admin role can enable the Notify manager assessment is overdue email notification.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assessment administrator tasks, Use, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable manager notifications

Users with the assessment\_admin role can enable the Notify manager assessment is overdue email notification.

## Before you begin

Role required: assessment\_admin or admin

## About this task

This notification sends emails to assessors' managers when assessors do not complete their assigned assessments on time. For more information, see the table of assessment notifications. You must enable or disable this email notification separately for each metric type.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Types**.

2.  Open a metric type.

3.  Select the **Notify if overdue** check box.

    ![The Notify if overdue option](../image/NotifyIfOverdue.png)

    To disable manager notifications, clear the check box.

4.  Save the record.

    **Note:** The assessor's user record must have a manager specified in the **Manager** field to use this notification. You might need to configure the form to use this field.


-   **[Assessment notifications](../../assessments/reference/r_AssessmentNotifications.md)**  
You can configure the system to send email notifications for assessments.
-   **[Assessment notification workflow](../reference/r_AssessmentNotificationWorkflow.md)**  
The system sends assessment notifications according to the Notify assessment user workflow. Users with the workflow\_admin, workflow\_creator, or workflow\_publisher roles can view workflows.

**Parent Topic:**[Assessment administrator tasks](../../assessments/concept/c_AssessmentProcess.md)

