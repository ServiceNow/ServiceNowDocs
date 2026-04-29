---
title: Assessment notifications
description: You can configure the system to send email notifications for assessments.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable manager notifications, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Assessment notifications

You can configure the system to send email notifications for assessments.

You can configure any of the following types of notification during the process of generating assessable records:

-   Notify assessment user: This messages notifies you of an assigned an assessment and includes the [type](../concept/c_MetricTypesAndAssessableRecords.md), the due date, and basic instructions. The message also contains a link to the record where you take the assessment.

    **Note:** If a user has a pending assessment, then the system will not generate another instance of the same assessment.

-   Remind assessment user: This message reminds you of the due date if half the time passes and you have not completed the assessment. The message content is the same as the first notification.
-   Notify manager assessment is overdue: If you do not complete an assessment by the due date, the system may send a notification to your manager, depending on configuration.

**Note:** By default, the system runs a script every 30 days to cancel expired assessment and survey instances that are in the **Work in progress** or **Ready to take** states.

**Parent Topic:**[Enable manager notifications](../../notification/task/t_EnablingManagerNotifications.md)

**Related topics**  


[Create metric types and generate assessable records](../task/t_CreatMetricTypesAndGenAssessRecs.md)

[Event scheduling](https://www.servicenow.com/docs/access?context=c_ScheduleEvents&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

